---
UID: NF:winsatcominterfacei.IQueryRecentWinSATAssessment.get_XML
title: IQueryRecentWinSATAssessment::get_XML (winsatcominterfacei.h)
description: Retrieves data from the XML assessment document by using the specified XPath. The query is run against the most recent formal assessment in the WinSAT data store.
helpviewer_keywords: ["IQueryRecentWinSATAssessment interface [WinSAT]","XML property","IQueryRecentWinSATAssessment.XML","IQueryRecentWinSATAssessment.get_XML","IQueryRecentWinSATAssessment::XML","IQueryRecentWinSATAssessment::get_XML","XML property [WinSAT]","XML property [WinSAT]","IQueryRecentWinSATAssessment interface","get_XML","winsat.iqueryrecentwinsatassessment_xml","winsatcominterfacei/IQueryRecentWinSATAssessment::XML","winsatcominterfacei/IQueryRecentWinSATAssessment::get_XML"]
old-location: winsat\iqueryrecentwinsatassessment_xml.htm
tech.root: WinSAT
ms.assetid: f8a1c664-bea3-4505-bcf0-2b8715dbe7dd
ms.date: 12/05/2018
ms.keywords: IQueryRecentWinSATAssessment interface [WinSAT],XML property, IQueryRecentWinSATAssessment.XML, IQueryRecentWinSATAssessment.get_XML, IQueryRecentWinSATAssessment::XML, IQueryRecentWinSATAssessment::get_XML, XML property [WinSAT], XML property [WinSAT],IQueryRecentWinSATAssessment interface, get_XML, winsat.iqueryrecentwinsatassessment_xml, winsatcominterfacei/IQueryRecentWinSATAssessment::XML, winsatcominterfacei/IQueryRecentWinSATAssessment::get_XML
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
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryRecentWinSATAssessment::get_XML
 - winsatcominterfacei/IQueryRecentWinSATAssessment::get_XML
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IQueryRecentWinSATAssessment.XML
 - IQueryRecentWinSATAssessment.get_XML
---

# IQueryRecentWinSATAssessment::get_XML


## -description

<p class="CCE_Message">[IQueryRecentWinSATAssessment::XML may be altered or unavailable for releases after Windows 8.1.]

Retrieves data from the XML assessment document by using the specified XPath. The query is run against the most recent formal assessment in the WinSAT data store.

This property is read-only.

## -parameters

## -remarks

You can use this method to retrieve details of the assessment that are not available in the summary information provided through the API. For details about all the information available in an assessment, see the <a href="/windows/desktop/WinSAT/winsat-schema">WinSAT Schema</a>.

The first formal assessment is run when you initially set up your computer. The initial assessment will remain in the data store for the life of the data store. The WinSAT data store can contain up to 100 formal assessments. When the store reaches capacity, WinSAT will delete the oldest assessment (but not the initial assessment) in the data store for each new formal assessment that is run.

The WinSAT data store contains only formal assessments. If you want to retrieve assessment data from ad hoc assessments, you must save the results to an XML file when you run the assessment (see the <b>-xml</b> command-line argument for details). You can then use the members of the <b>IXMLDOMDocument2</b> interface to query data from the ad hoc assessment.

To retrieve summary information about the assessment, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info">IQueryRecentWinSATAssessment::get_Info</a> method. To retrieve summary information for a subcomponent of the assessment, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.


#### Examples

The following example shows how to use an XPath query to get data from the most recent formal assessment.


```cpp
#include <windows.h>
#include <stdio.h>
#include <winsatcominterfacei.h>

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

    // Get an instance to the most recent formal assessment.
    hr = CoCreateInstance(__uuidof(CQueryWinSAT),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IQueryRecentWinSATAssessment),
        (void**)&pAssessment);

    if (FAILED(hr))
    {
        wprintf(L"Failed to create an instance of IQueryRecentWinSATAssessment. Failed with 0x%x.\n", hr);
        goto cleanup;
    }

    // Query the assessment for the nodes that match the XPath expression.
    hr = pAssessment->get_XML(bstrXPath, NULL, &pNodes);
    if (FAILED(hr))
    {
        wprintf(L"pAssessment->get_XML failed with 0x%x.\n", hr);
        goto cleanup;
    }

    hr = pNodes->get_length(&NodeCount);
    wprintf(L"There were %d results found for the XPath query.\n\n", NodeCount);

    // Loop through the results.
    for (long i = 0; i < NodeCount; i++)
    {
        hr = pNodes->nextNode(&pNode);
        if (pNode)
        {
            hr = pNode->get_text(&bstrTime);
            if (S_OK == hr)
            {
                wprintf(L"Total runtime of the assessment: %s\n", bstrTime);
                SysFreeString(bstrTime);
            }
            else
            {
                wprintf(L"pNode->get_text failed with 0x%x.\n", hr);
                goto cleanup;
            }

            pNode->Release();
            pNode = NULL;
        }
        else
        {
            wprintf(L"pNodes->nextNode failed with 0x%x.\n", hr);
            goto cleanup;
        }
    }

cleanup:

    if (pAssessment)
        pAssessment->Release();

    if (pNodes)
        pNodes->Release();

    if (bstrXPath)
        SysFreeString(bstrXPath);

    CoUninitialize();
}

```

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml">IQueryAllWinSATAssessments::AllXML</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryrecentwinsatassessment">IQueryRecentWinSATAssessment</a>