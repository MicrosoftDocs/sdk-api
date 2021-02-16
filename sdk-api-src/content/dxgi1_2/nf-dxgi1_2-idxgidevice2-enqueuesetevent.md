---
UID: NF:dxgi1_2.IDXGIDevice2.EnqueueSetEvent
title: IDXGIDevice2::EnqueueSetEvent (dxgi1_2.h)
description: Flushes any outstanding rendering commands and sets the specified event object to the signaled state after all previously submitted rendering commands complete.
helpviewer_keywords: ["EnqueueSetEvent","EnqueueSetEvent method [DXGI]","EnqueueSetEvent method [DXGI]","IDXGIDevice2 interface","IDXGIDevice2 interface [DXGI]","EnqueueSetEvent method","IDXGIDevice2.EnqueueSetEvent","IDXGIDevice2::EnqueueSetEvent","direct3ddxgi.idxgidevice2_enqueuesetevent","dxgi1_2/IDXGIDevice2::EnqueueSetEvent"]
old-location: direct3ddxgi\idxgidevice2_enqueuesetevent.htm
tech.root: direct3ddxgi
ms.assetid: CECF3ED6-A025-48C4-A7E2-971B86A262F0
ms.date: 12/05/2018
ms.keywords: EnqueueSetEvent, EnqueueSetEvent method [DXGI], EnqueueSetEvent method [DXGI],IDXGIDevice2 interface, IDXGIDevice2 interface [DXGI],EnqueueSetEvent method, IDXGIDevice2.EnqueueSetEvent, IDXGIDevice2::EnqueueSetEvent, direct3ddxgi.idxgidevice2_enqueuesetevent, dxgi1_2/IDXGIDevice2::EnqueueSetEvent
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDevice2::EnqueueSetEvent
 - dxgi1_2/IDXGIDevice2::EnqueueSetEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDevice2.EnqueueSetEvent
---

# IDXGIDevice2::EnqueueSetEvent


## -description

Flushes any outstanding rendering commands and sets the specified event object to the signaled state after all previously submitted rendering commands complete.

## -parameters

### -param hEvent [in]

A handle to the event object. The <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> function returns this handle. All types of event objects (manual-reset, auto-reset, and so on) are supported.

The handle must have the EVENT_MODIFY_STATE access right. For more information about access rights, see <a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

## -returns

Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:

<ul>
<li><b>E_OUTOFMEMORY</b> if insufficient memory is available to complete the operation.</li>
<li><b>E_INVALIDARG</b> if the parameter was validated and determined to be incorrect.</li>
</ul>
<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>EnqueueSetEvent</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

<b>EnqueueSetEvent</b> calls the <a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> function on the event object after all previously submitted rendering commands complete or the device is removed.

After an application calls <b>EnqueueSetEvent</b>, it  can immediately call the <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> function to put itself to sleep until rendering commands complete.

You cannot use <b>EnqueueSetEvent</b> to determine work completion that is associated with presentation (<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a>); instead, we recommend that you use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getframestatistics">IDXGISwapChain::GetFrameStatistics</a>.


#### Examples

The following example code shows how to use <b>EnqueueSetEvent</b>.


```
void BlockingFinish( IDXGIDevice2* pDevice ) 
{
    // Create a manual-reset event object. 
    hEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        FALSE
        ); 

    if (hEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    pDevice->EnqueueSetEvent(hEvent);    

    DWORD dwWaitResult = WaitForSingleObject( 
        hEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            // Commands completed
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    CloseHandle(hEvent);
}

```

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>