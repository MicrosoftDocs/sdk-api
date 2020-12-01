---
UID: NF:winsatcominterfacei.IInitiateWinSATAssessment.InitiateFormalAssessment
title: IInitiateWinSATAssessment::InitiateFormalAssessment (winsatcominterfacei.h)
description: Initiates a formal assessment.
helpviewer_keywords: ["IInitiateWinSATAssessment interface [WinSAT]","InitiateFormalAssessment method","IInitiateWinSATAssessment.InitiateFormalAssessment","IInitiateWinSATAssessment::InitiateFormalAssessment","InitiateFormalAssessment","InitiateFormalAssessment method [WinSAT]","InitiateFormalAssessment method [WinSAT]","IInitiateWinSATAssessment interface","winsat.iinitiatewinsatassessment_initiateformalassessment","winsatcominterfacei/IInitiateWinSATAssessment::InitiateFormalAssessment"]
old-location: winsat\iinitiatewinsatassessment_initiateformalassessment.htm
tech.root: WinSAT
ms.assetid: 9425e41c-fe03-4c94-a5eb-686775b5fce7
ms.date: 12/05/2018
ms.keywords: IInitiateWinSATAssessment interface [WinSAT],InitiateFormalAssessment method, IInitiateWinSATAssessment.InitiateFormalAssessment, IInitiateWinSATAssessment::InitiateFormalAssessment, InitiateFormalAssessment, InitiateFormalAssessment method [WinSAT], InitiateFormalAssessment method [WinSAT],IInitiateWinSATAssessment interface, winsat.iinitiatewinsatassessment_initiateformalassessment, winsatcominterfacei/IInitiateWinSATAssessment::InitiateFormalAssessment
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
 - IInitiateWinSATAssessment::InitiateFormalAssessment
 - winsatcominterfacei/IInitiateWinSATAssessment::InitiateFormalAssessment
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
 - IInitiateWinSATAssessment.InitiateFormalAssessment
---

# IInitiateWinSATAssessment::InitiateFormalAssessment


## -description

<p class="CCE_Message">[IInitiateWinSATAssessment::InitiateFormalAssessment may be altered or unavailable for releases after Windows 8.1.]

Initiates a formal assessment.

## -parameters

### -param pCallbacks [in, optional]

An <a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents">IWinSATInitiateEvents</a> interface that you implement to receive notification when the assessment finishes or makes progress. Can be <b>NULL</b> if you do not want to receive notifications.

### -param callerHwnd [in, optional]

The window handle of your client. The handle is used to center the WinSAT dialog boxes. If <b>NULL</b>, the dialog boxes are centered on the desktop.

## -returns

This method can return one of these values.


This following table lists some of the HRESULT values that this method returns.





<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
WinSAT successfully started. To determine if the assessment ran successfully, implement the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iwinsatinitiateevents-winsatcomplete">IWinSATInitiateEvents::WinSATComplete</a> method and check the value of the <i>hresult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINSAT_ERROR_WINSAT_DOES_NOT_EXIST</b></dt>
<dt>0x80040011</dt>
</dl>
</td>
<td width="60%">
Could not find the WinSAT program where expected.

</td>
</tr>
</table>

## -remarks

You typically run a formal assessment to assess all subcomponents of the computer, whereas an ad hoc assessment assesses one subcomponent of the computer. To run an ad hoc assessment, call the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment">IInitiateWinSATAssessment::InitiateAssessment</a> method.

To get the results of a formal assessment, use the <a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryrecentwinsatassessment">IQueryRecentWinSATAssessment</a> interface.  

If you call this function from a Windows application, implement the <a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents">IWinSATInitiateEvents</a> interface so that you can display progress information and receive notification when the assessment is complete. For a Windows console application, showing progress is not necessary because WinSAT writes progress information to the console window.

Note that WinSAT requires administrator privileges to run. If the user does not have administrator privileges, WinSAT will display a dialog box that asks for credentials.   


#### Examples

The following example shows how to run a formal assessment and receive notification of its progress.  


```cpp
#include <windows.h>
#include <stdio.h>
#include <conio.h>  // For kbhit()
#include <winsatcominterfacei.h>

#pragma comment(lib, "ole32.lib")

// Class that implements IWinSATInitiateEvents. Implement this class to
// get progress information and completion notification.
class CWinSATCallbacks : public IWinSATInitiateEvents
{
    LONG m_lRefCount;

public:

    // Constructor, Destructor
    CWinSATCallbacks() {m_lRefCount = 1;};
    ~CWinSATCallbacks() {};

    // IUnknown methods
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    // IWinSATInitiateEvents methods
    HRESULT __stdcall WinSATComplete(HRESULT hr, LPCWSTR description);
    HRESULT __stdcall WinSATUpdate(UINT currentTick, UINT tickTotal, LPCWSTR currentState);
};


HRESULT CWinSATCallbacks::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IWinSATInitiateEvents)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL;
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CWinSATCallbacks::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CWinSATCallbacks::Release() 
{
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

// Is called when WinSAT completes the assessment or an error occurs.
HRESULT CWinSATCallbacks::WinSATComplete(HRESULT hr, LPCWSTR description)
{
    if (SUCCEEDED(hr))
    {
        wprintf(L"\n*** %s", description);
    }
    else
    {
        wprintf(L"\n*** The assessment failed with 0x%x (%s)\n", hr, description);
    }

    return S_OK;
}

// Is called when the assessment makes progress. Indicates the percentage of the assessment
// that is complete and the current component being assessed.
HRESULT CWinSATCallbacks::WinSATUpdate(UINT currentTick, UINT tickTotal, LPCWSTR currentState)
{
    // Typically, you would provide the tick values to a ProgressBar control.

    if (tickTotal > 0)
    {
        wprintf(L"\n*** Percent complete: %u%%\n", 100*currentTick/tickTotal);
        wprintf(L"*** Currently assessing: %s\n\n", currentState);
    }

    return S_OK;
}

void main(void)
{
    HRESULT hr = S_OK;
    IInitiateWinSATAssessment* pAssessment = NULL;
    CWinSATCallbacks* pCallbacks = NULL;  // Class that implements IWinSATInitiateEvents

    CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    // Get an instance of the assessment interface.
    hr = CoCreateInstance(__uuidof(CInitiateWinSAT),
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          __uuidof(IInitiateWinSATAssessment),
                          (void**)&pAssessment);

    if (FAILED(hr))
    {
        wprintf(L"Failed to create an instance of IInitiateWinSATAssessment. Failed with 0x%x.\n", hr);
        goto cleanup;
    }

    wprintf(L"Running formal assessment... hit any key when complete.\n");

    pCallbacks = new CWinSATCallbacks();
    if (NULL == pCallbacks)
    {
        wprintf(L"Failed to create an instance of the CWinSATCallbacks class.\n");
        goto cleanup;
    }

    // Run the formal assessment.
    hr = pAssessment->InitiateFormalAssessment(pCallbacks, NULL);
    if (FAILED(hr))
    {
        // This is a failure to start WinSAT. If WinSAT fails while running, 
        // your implementation of the IWinSATInitiateEvents::WinSATComplete 
        // method will receive the failure code.
        wprintf(L"InitiateFormalAssessment failed with 0x%x.\n", hr);
        goto cleanup;
    }

    while (!_kbhit())
        Sleep(10);

cleanup:

    if (pAssessment)
        pAssessment->Release();

    if (pCallbacks)
        pCallbacks->Release();

    CoUninitialize();
}

```

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment">IInitiateWinSATAssessment::InitiateAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iqueryrecentwinsatassessment">IQueryRecentWinSATAssessment</a>