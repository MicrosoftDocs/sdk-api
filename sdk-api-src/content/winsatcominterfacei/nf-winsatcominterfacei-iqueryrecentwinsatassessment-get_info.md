---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IQueryRecentWinSATAssessment::get_Info


## -description


<p class="CCE_Message">[IQueryRecentWinSATAssessment::Info may be altered or unavailable for releases after Windows 8.1.]

Retrieves an interface that provides information about the results of the most recent formal assessment, for example, the base score and the date that the assessment was run.

This property is read-only.


## -parameters


## -remarks



To retrieve summary information for a subcomponent of the assessment, call the <a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">IProvideWinSATResultsInfo::GetAssessmentInfo</a> method.


#### Examples

The following example shows how to get the summary information for the most recent formal assessment.  The example gets the assessment date, base score, and state information.

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
    IProvideWinSATResultsInfo* pResults = NULL;
    float baseScore = 0.0;
    WINSAT_ASSESSMENT_STATE state;
    VARIANT vAssessmentDate;
    SYSTEMTIME st;

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

    // Get the summary information for the assessment.
    hr = pAssessment-&gt;get_Info(&amp;pResults);
    if (FAILED(hr))
    {
        wprintf(L"pAssessment-&gt;get_Info failed with 0x%x.\n", hr);
        goto cleanup;
    }

    // Get the state of the assessment. If the state is valid,
    // print the date of the assessment and the base score.
    hr = pResults-&gt;get_AssessmentState(&amp;state);
    if (FAILED(hr))
    {
        wprintf(L"pResults-&gt;get_AssessmentState failed with 0x%x.\n", hr);
        goto cleanup;
    }

    switch(state)
    {
        case WINSAT_ASSESSMENT_STATE_UNKNOWN:
            wprintf(L"The state of the assessment is unknown.\n");
            break;

        case WINSAT_ASSESSMENT_STATE_VALID:
        case WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE:
            hr = pResults-&gt;get_AssessmentDateTime(&amp;vAssessmentDate);
            if (FAILED(hr))
            {
                wprintf(L"pResults-&gt;get_AssessmentDateTime failed with 0x%x.\n", hr);
                break;
            }

            VariantTimeToSystemTime(vAssessmentDate.dblVal, &amp;st);
            wprintf(L"Assessment ran on %2d/%2d/%2d at %2d:%2d\n", 
                st.wMonth, st.wDay, st.wYear, st.wHour, st.wMinute);

            hr = pResults-&gt;get_SystemRating(&amp;baseScore);
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
                wprintf(L"pResults-&gt;get_SystemRating failed with 0x%x.\n", hr);
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
        pAssessment-&gt;Release();

    if (pResults)
        pResults-&gt;Release();

    VariantClear(&amp;vAssessmentDate);

    CoUninitialize();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6849d8b6-d192-4520-a737-39e22e14a70f">IQueryRecentWinSATAssessment</a>
 

 

