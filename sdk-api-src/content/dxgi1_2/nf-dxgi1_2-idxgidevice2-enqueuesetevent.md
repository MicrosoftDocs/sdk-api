---
UID: NF:dxgi1_2.IDXGIDevice2.EnqueueSetEvent
title: IDXGIDevice2::EnqueueSetEvent
author: windows-sdk-content
description: Flushes any outstanding rendering commands and sets the specified event object to the signaled state after all previously submitted rendering commands complete.
old-location: direct3ddxgi\idxgidevice2_enqueuesetevent.htm
old-project: direct3ddxgi
ms.assetid: CECF3ED6-A025-48C4-A7E2-971B86A262F0
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: EnqueueSetEvent, EnqueueSetEvent method [DXGI], EnqueueSetEvent method [DXGI],IDXGIDevice2 interface, IDXGIDevice2 interface [DXGI],EnqueueSetEvent method, IDXGIDevice2.EnqueueSetEvent, IDXGIDevice2::EnqueueSetEvent, direct3ddxgi.idxgidevice2_enqueuesetevent, dxgi1_2/IDXGIDevice2::EnqueueSetEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice2::EnqueueSetEvent


## -description


Flushes any outstanding rendering commands and sets the specified event object to the signaled state after all previously submitted rendering commands complete.


## -parameters




### -param hEvent [in]

A handle to the event object. The <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> function returns this handle. All types of event objects (manual-reset, auto-reset, and so on) are supported.

The handle must have the EVENT_MODIFY_STATE access right. For more information about access rights, see <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


## -returns



Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:

<ul>
<li><b>E_OUTOFMEMORY</b> if insufficient memory is available to complete the operation.</li>
<li><b>E_INVALIDARG</b> if the parameter was validated and determined to be incorrect.</li>
</ul>
<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>EnqueueSetEvent</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



<b>EnqueueSetEvent</b> calls the <a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a> function on the event object after all previously submitted rendering commands complete or the device is removed.

After an application calls <b>EnqueueSetEvent</b>, it  can immediately call the <a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a> function to put itself to sleep until rendering commands complete.

You cannot use <b>EnqueueSetEvent</b> to determine work completion that is associated with presentation (<a href="https://msdn.microsoft.com/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>); instead, we recommend that you use <a href="https://msdn.microsoft.com/library/Bb174573(v=VS.85).aspx">IDXGISwapChain::GetFrameStatistics</a>.


#### Examples

The following example code shows how to use <b>EnqueueSetEvent</b>.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>void BlockingFinish( IDXGIDevice2* pDevice ) 
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

    pDevice-&gt;EnqueueSetEvent(hEvent);    

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>
 

 

