---
UID: NF:winsatcominterfacei.IQueryAllWinSATAssessments.get_AllXML
title: IQueryAllWinSATAssessments::get_AllXML (winsatcominterfacei.h)
description: Retrieves data from the formal XML assessment documents using the specified XPath. The query is run against all formal assessments in the WinSAT data store.
helpviewer_keywords: ["AllXML property [WinSAT]","AllXML property [WinSAT]","IQueryAllWinSATAssessments interface","IQueryAllWinSATAssessments interface [WinSAT]","AllXML property","IQueryAllWinSATAssessments.AllXML","IQueryAllWinSATAssessments.get_AllXML","IQueryAllWinSATAssessments::AllXML","IQueryAllWinSATAssessments::get_AllXML","get_AllXML","winsat.iqueryallwinsatassessments_allxml","winsatcominterfacei/IQueryAllWinSATAssessments::AllXML","winsatcominterfacei/IQueryAllWinSATAssessments::get_AllXML"]
old-location: winsat\iqueryallwinsatassessments_allxml.htm
tech.root: WinSAT
ms.assetid: a43aee18-642f-44d9-a116-ffc762cec80a
ms.date: 12/05/2018
ms.keywords: AllXML property [WinSAT], AllXML property [WinSAT],IQueryAllWinSATAssessments interface, IQueryAllWinSATAssessments interface [WinSAT],AllXML property, IQueryAllWinSATAssessments.AllXML, IQueryAllWinSATAssessments.get_AllXML, IQueryAllWinSATAssessments::AllXML, IQueryAllWinSATAssessments::get_AllXML, get_AllXML, winsat.iqueryallwinsatassessments_allxml, winsatcominterfacei/IQueryAllWinSATAssessments::AllXML, winsatcominterfacei/IQueryAllWinSATAssessments::get_AllXML
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
 - IQueryAllWinSATAssessments::get_AllXML
 - winsatcominterfacei/IQueryAllWinSATAssessments::get_AllXML
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
 - IQueryAllWinSATAssessments.AllXML
 - IQueryAllWinSATAssessments.get_AllXML
---

# IQueryAllWinSATAssessments::get_AllXML


## -description

<p class="CCE_Message">[IQueryAllWinSATAssessments::AllXML may be altered or unavailable for releases after Windows 8.1.]

Retrieves data from the formal XML assessment documents using the specified XPath. The query is run against all formal assessments in the WinSAT data store.

This property is read-only.

## -parameters

## -remarks

You can use this method to retrieve details of the assessment that are not available in the summary information provided through the API. For details about all the information available in an assessment, see the <a href="/windows/desktop/WinSAT/winsat-schema">WinSAT Schema</a>.

The first formal assessment is run when you initially set up your computer. The initial assessment will remain in the data store for the life of the data store. The WinSAT data store can contain up to 100 formal assessments. When the store reaches capacity, WinSAT will delete the oldest assessment (but not the initial assessment) in the data store for each new formal assessment that is run.

The WinSAT data store contains only formal assessments. If you want to retrieve assessment data from ad hoc assessments, you must save the results to an XML file when you run the assessment (see the <b>-xml</b> command-line argument for details). You can then use the members of the <b>IXMLDOMDocument2</b> interface to query data from the ad hoc assessment.

The order in which the assessments are returned is arbitrary.


#### Examples

The following example shows how to use an XPath query to get data from each of the formal assessments in the assessment store.


```cpp
#include <windows.h>
#include <stdio.h>
#include <comutil.h>
#include <winsatcominterfacei.h>

#pragma comment(lib, "comsupp.lib") // For _bstr_t

void main(void)
{
    HRESULT hr = S_OK;
    IQueryAllWinSATAssessments* pAssessment;
    IXMLDOMNodeList* pNodes = NULL;
    IXMLDOMNode* pMemory = NULL;
    IXMLDOMNode* pNode = NULL;
    _bstr_t bstrXPath = L"WinsatAssessments/WinSAT/SystemConfig/Memory";
    _bstr_t bstrAvailableRAM;
    _bstr_t bstrTotalRAM;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    // Get an instance to the most recent formal assessment.
    hr = CoCreateInstance(__uuidof(CQueryAllWinSAT),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IQueryAllWinSATAssessments),
        (void**)&pAssessment);

    if (FAILED(hr))
    {
        wprintf(L"Failed to create an instance of IQueryAllWinSATAssessments. Failed with 0x%x.\n", hr);
        goto cleanup;
    }

    // Query the assessments for the memory nodes.
    hr = pAssessment->get_AllXML(bstrXPath, NULL, &pNodes);
    if (FAILED(hr))
    {
        wprintf(L"pAssessment->get_XML failed with 0x%x.\n", hr);
        goto cleanup;
    }

    hr = pNodes->nextNode(&pMemory);

    // Loop through the memory nodes and get available and total memory size
    // values and print them.
    while (pMemory)
    {
        hr = pMemory->selectSingleNode(L"TotalPhysical/Size", &pNode);
        if (FAILED(hr))
        {
            wprintf(L"pMemory->selectSingleNode(TotalPhysical/Size) failed with 0x%x.\n", hr);
            goto cleanup;
        }

        hr = pNode->get_text(bstrTotalRAM.GetAddress());
        if (FAILED(hr))
        {
            wprintf(L"pNode->get_text(bstrTotalRAM) failed with 0x%x.\n", hr);
            goto cleanup;
        }

        pNode->Release();
        pNode = NULL;

        hr = pMemory->selectSingleNode(L"AvailablePhysical/Size", &pNode);
        if (FAILED(hr))
        {
            wprintf(L"pMemory->selectSingleNode(AvailablePhysical/Size) failed with 0x%x.\n", hr);
            goto cleanup;
        }

        hr = pNode->get_text(bstrAvailableRAM.GetAddress());
        if (FAILED(hr))
        {
            wprintf(L"pNode->get_text(bstrAvailableRAM) failed with 0x%x.\n", hr);
            goto cleanup;
        }

        pNode->Release();
        pNode = NULL;

        wprintf(L"Available RAM: %s of %s\n", bstrAvailableRAM.GetBSTR(), bstrTotalRAM.GetBSTR());

        pMemory->Release();
        pMemory = NULL;

        hr = pNodes->nextNode(&pMemory);
    }

cleanup:

    if (pAssessment)
        pAssessment->Release();

    if (pNodes)
        pNodes->Release();

    if (pMemory)
        pMemory->Release();

    if (pNode)
        pNode->Release();

    CoUninitialize();
}

```

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryallwinsatassessments">IQueryAllWinSATAssessments</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml">IQueryRecentWinSATAssessment::XML</a>