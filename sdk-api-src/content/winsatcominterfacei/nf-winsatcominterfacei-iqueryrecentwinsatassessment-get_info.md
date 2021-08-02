---
UID: NF:winsatcominterfacei.IQueryRecentWinSATAssessment.get_Info
title: IQueryRecentWinSATAssessment::get_Info (winsatcominterfacei.h)
description: Retrieves an interface that provides information about the results of the most recent formal assessment, for example, the base score and the date that the assessment was run.
helpviewer_keywords: ["IQueryRecentWinSATAssessment interface [WinSAT]","Info property","IQueryRecentWinSATAssessment.Info","IQueryRecentWinSATAssessment.get_Info","IQueryRecentWinSATAssessment::Info","IQueryRecentWinSATAssessment::get_Info","Info property [WinSAT]","Info property [WinSAT]","IQueryRecentWinSATAssessment interface","get_Info","winsat.iqueryrecentwinsatassessment_info","winsatcominterfacei/IQueryRecentWinSATAssessment::Info","winsatcominterfacei/IQueryRecentWinSATAssessment::get_Info"]
old-location: winsat\iqueryrecentwinsatassessment_info.htm
tech.root: WinSAT
ms.assetid: 11697416-aa4d-4724-bd63-8d123e2b32cb
ms.date: 12/05/2018
ms.keywords: IQueryRecentWinSATAssessment interface [WinSAT],Info property, IQueryRecentWinSATAssessment.Info, IQueryRecentWinSATAssessment.get_Info, IQueryRecentWinSATAssessment::Info, IQueryRecentWinSATAssessment::get_Info, Info property [WinSAT], Info property [WinSAT],IQueryRecentWinSATAssessment interface, get_Info, winsat.iqueryrecentwinsatassessment_info, winsatcominterfacei/IQueryRecentWinSATAssessment::Info, winsatcominterfacei/IQueryRecentWinSATAssessment::get_Info
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
 - IQueryRecentWinSATAssessment::get_Info
 - winsatcominterfacei/IQueryRecentWinSATAssessment::get_Info
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
 - IQueryRecentWinSATAssessment.Info
 - IQueryRecentWinSATAssessment.get_Info
---

# IQueryRecentWinSATAssessment::get_Info


## -description

<p class="CCE_Message">[IQueryRecentWinSATAssessment::Info may be altered or unavailable for releases after Windows 8.1.]

Retrieves an interface that provides information about the results of the most recent formal assessment, for example, the base score and the date that the assessment was run.

This property is read-only.

## -parameters

## -remarks

To retrieve summary information for a subcomponent of the assessment, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.


#### Examples

The following example shows how to get the summary information for the most recent formal assessment.  The example gets the assessment date, base score, and state information.


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
    IProvideWinSATResultsInfo* pResults = NULL;
    float baseScore = 0.0;
    WINSAT_ASSESSMENT_STATE state;
    VARIANT vAssessmentDate;
    SYSTEMTIME st;

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

    // Get the summary information for the assessment.
    hr = pAssessment->get_Info(&pResults);
    if (FAILED(hr))
    {
        wprintf(L"pAssessment->get_Info failed with 0x%x.\n", hr);
        goto cleanup;
    }

    // Get the state of the assessment. If the state is valid,
    // print the date of the assessment and the base score.
    hr = pResults->get_AssessmentState(&state);
    if (FAILED(hr))
    {
        wprintf(L"pResults->get_AssessmentState failed with 0x%x.\n", hr);
        goto cleanup;
    }

    switch(state)
    {
        case WINSAT_ASSESSMENT_STATE_UNKNOWN:
            wprintf(L"The state of the assessment is unknown.\n");
            break;

        case WINSAT_ASSESSMENT_STATE_VALID:
        case WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE:
            hr = pResults->get_AssessmentDateTime(&vAssessmentDate);
            if (FAILED(hr))
            {
                wprintf(L"pResults->get_AssessmentDateTime failed with 0x%x.\n", hr);
                break;
            }

            VariantTimeToSystemTime(vAssessmentDate.dblVal, &st);
            wprintf(L"Assessment ran on %2d/%2d/%2d at %2d:%2d\n", 
                st.wMonth, st.wDay, st.wYear, st.wHour, st.wMinute);

            hr = pResults->get_SystemRating(&baseScore);
            if (SUCCEEDED(hr))
            {
                wprintf(L"The base score for the computer is %.1f\n", baseScore);

                if (WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE == state)
                {
                    wprintf(L"Note that the hardware configuration of the computer has changed\n"
                            L"since the assessment was run; the score reflects the prior configuration.");
                }
            }
            else
            {
                wprintf(L"pResults->get_SystemRating failed with 0x%x.\n", hr);
            }
            break;

        case WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE:
            wprintf(L"A formal assessment has not run on the computer.\n");
            break;

        case WINSAT_ASSESSMENT_STATE_INVALID:
            wprintf(L"The assessment data is not valid.\n");
            break;

        default:
            wprintf(L"The assessment state value is not valid.\n");
    }

cleanup:

    if (pAssessment)
        pAssessment->Release();

    if (pResults)
        pResults->Release();

    VariantClear(&vAssessmentDate);

    CoUninitialize();
}

```

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryrecentwinsatassessment">IQueryRecentWinSATAssessment</a>