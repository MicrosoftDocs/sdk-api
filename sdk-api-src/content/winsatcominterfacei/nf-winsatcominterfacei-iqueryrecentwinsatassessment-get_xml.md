---
UID: NF:winsatcominterfacei.IQueryRecentWinSATAssessment.get_XML
title: IQueryRecentWinSATAssessment::get_XML
author: windows-sdk-content
description: Retrieves data from the XML assessment document by using the specified XPath. The query is run against the most recent formal assessment in the WinSAT data store.
old-location: winsat\iqueryrecentwinsatassessment_xml.htm
old-project: WinSAT
ms.assetid: f8a1c664-bea3-4505-bcf0-2b8715dbe7dd
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IQueryRecentWinSATAssessment interface [WinSAT],XML property, IQueryRecentWinSATAssessment.XML, IQueryRecentWinSATAssessment.get_XML, IQueryRecentWinSATAssessment::XML, IQueryRecentWinSATAssessment::get_XML, XML property [WinSAT], XML property [WinSAT],IQueryRecentWinSATAssessment interface, get_XML, winsat.iqueryrecentwinsatassessment_xml, winsatcominterfacei/IQueryRecentWinSATAssessment::XML, winsatcominterfacei/IQueryRecentWinSATAssessment::get_XML
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Winsatapi.dll
api_name:
-	IQueryRecentWinSATAssessment.XML
-	IQueryRecentWinSATAssessment.get_XML
product: Windows
targetos: Windows
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IQueryRecentWinSATAssessment::get_XML


## -description


<p class="CCE_Message">[IQueryRecentWinSATAssessment::XML may be altered or unavailable for releases after Windows 8.1.]

Retrieves data from the XML assessment document by using the specified XPath. The query is run against the most recent formal assessment in the WinSAT data store.

This property is read-only.


## -parameters


## -remarks



You can use this method to retrieve details of the assessment that are not available in the summary information provided through the API. For details about all the information available in an assessment, see the <a href="https://msdn.microsoft.com/da497f3b-f5a2-401e-8230-937362ecf4f2">WinSAT Schema</a>.

The first formal assessment is run when you initially set up your computer. The initial assessment will remain in the data store for the life of the data store. The WinSAT data store can contain up to 100 formal assessments. When the store reaches capacity, WinSAT will delete the oldest assessment (but not the initial assessment) in the data store for each new formal assessment that is run.

The WinSAT data store contains only formal assessments. If you want to retrieve assessment data from ad hoc assessments, you must save the results to an XML file when you run the assessment (see the <b>-xml</b> command-line argument for details). You can then use the members of the <b>IXMLDOMDocument2</b> interface to query data from the ad hoc assessment.

To retrieve summary information about the assessment, call the <a href="https://msdn.microsoft.com/11697416-aa4d-4724-bd63-8d123e2b32cb">IQueryRecentWinSATAssessment::get_Info</a> method. To retrieve summary information for a subcomponent of the assessment, call the <a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.


#### Examples

The following example shows how to use an XPath query to get data from the most recent formal assessment.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;winsatcominterfacei.h&gt;

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

void main(void)
{
    HRESULT hr = S_OK;
    IQueryRecentWinSATAssessment* pAssessment;
    IXMLDOMNodeList* pNodes = NULL;
    IXMLDOMNode* pNode = NULL;
    long NodeCount = 0;
    BSTR bstrXPath = SysAllocString(L"WinSAT/TotalRunTime/Description");
    BSTR bstrTime = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    // Get an instance to the most recent formal assessmenet.
    hr = CoCreateInstance(__uuidof(CQueryWinSAT),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IQueryRecentWinSATAssessment),
        (void**)&amp;pAssessment);

    if (FAILED(hr))
    {
        wprintf(L"Failed to create an instance of IQueryRecentWinSATAssessment. Failed with 0x%x.\n", hr);
        goto cleanup;
    }

    // Query the assessment for the nodes that match the XPath expression.
    hr = pAssessment-&gt;get_XML(bstrXPath, NULL, &amp;pNodes);
    if (FAILED(hr))
    {
        wprintf(L"pAssessment-&gt;get_XML failed with 0x%x.\n", hr);
        goto cleanup;
    }

    hr = pNodes-&gt;get_length(&amp;NodeCount);
    wprintf(L"There were %d results found for the XPath query.\n\n", NodeCount);

    // Loop through the results.
    for (long i = 0; i &lt; NodeCount; i++)
    {
        hr = pNodes-&gt;nextNode(&amp;pNode);
        if (pNode)
        {
            hr = pNode-&gt;get_text(&amp;bstrTime);
            if (S_OK == hr)
            {
                wprintf(L"Total runtime of the assessment: %s\n", bstrTime);
                SysFreeString(bstrTime);
            }
            else
            {
                wprintf(L"pNode-&gt;get_text failed with 0x%x.\n", hr);
                goto cleanup;
            }

            pNode-&gt;Release();
            pNode = NULL;
        }
        else
        {
            wprintf(L"pNodes-&gt;nextNode failed with 0x%x.\n", hr);
            goto cleanup;
        }
    }

cleanup:

    if (pAssessment)
        pAssessment-&gt;Release();

    if (pNodes)
        pNodes-&gt;Release();

    if (bstrXPath)
        SysFreeString(bstrXPath);

    CoUninitialize();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0b299477-50a4-4f61-a0e5-fdbae239503b">IInitiateWinSATAssessment</a>



<a href="https://msdn.microsoft.com/a43aee18-642f-44d9-a116-ffc762cec80a">IQueryAllWinSATAssessments::AllXML</a>



<a href="https://msdn.microsoft.com/6849d8b6-d192-4520-a737-39e22e14a70f">IQueryRecentWinSATAssessment</a>
 

 

