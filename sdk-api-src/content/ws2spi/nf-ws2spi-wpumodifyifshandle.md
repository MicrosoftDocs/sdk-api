---
UID: NF:ws2spi.WPUModifyIFSHandle
title: WPUModifyIFSHandle function
author: windows-sdk-content
description: The WPUModifyIFSHandle function receives a (possibly) modified IFS handle from Ws2_32.dll.
old-location: winsock\wpumodifyifshandle_2.htm
tech.root: winsock
ms.assetid: f58971eb-0948-4e16-a767-1d4cba9ec721
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WPUModifyIFSHandle, WPUModifyIFSHandle function [Winsock], _win32_wpumodifyifshandle_2, winsock.wpumodifyifshandle_2, ws2spi/WPUModifyIFSHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUModifyIFSHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WPUModifyIFSHandle function


## -description


The 
<b>WPUModifyIFSHandle</b> function receives a (possibly) modified IFS handle from Ws2_32.dll.


## -parameters




### -param dwCatalogEntryId [in]

Descriptor identifying the calling service provider.


### -param ProposedHandle [in]

IFS handle allocated by the provider.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, 
<b>WPUModifyIFSHandle</b> returns the modified socket handle. Otherwise, it returns INVALID_SOCKET, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The proposed handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>WPUModifyIFSHandle</b> handle allows the WS2_32.dll to streamline its internal operations by returning a possibly modified version of the supplied IFS handle. The returned handle is guaranteed to be indistinguishable from the proposed handle as far as the operating system is concerned. IFS providers must call this function before returning any newly created socket descriptor to a service provider. The service provider will only use the modified handle for any subsequent socket operations. This routine is only used by IFS providers whose socket descriptors are real IFS handles.


<div> </div><b>Layered Service Provider Considerations</b>

This procedure may also be used by a layered provider that is layered on top of a base IFS provider and wants to expose the base provider's socket handles as its own instead of creating them with a 
<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a> call. A layered provider that wishes to "pass through" the IFS socket handles it receives from the next layer in the chain can call 
<b>WPUModifyIFSHandle</b>, passing its own catalog entry ID as <i>dwCatalogEntryId</i>. This informs the Windows Sockets DLL that this layer, and not the next layer, should be the target for SPI calls involving that socket handle.

There are several limitations a layered provider should observe if it takes this approach.

<ul>
<li>The provider should expose base provider entry points for 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a> and 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a> in the procedure dispatch table it returns at the time of 
<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a> to make sure the Windows Sockets SPI client's access to these functions is as efficient as possible.</li>
<li>The provider cannot rely on its 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a> and 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a> functions being invoked for all I/O, particularly in the case of the I/O system functions <a href="https://msdn.microsoft.com/en-us/library/Aa365467(v=VS.85).aspx">ReadFile</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa365747(v=VS.85).aspx">WriteFile</a>. These functions would bypass the layered provider and invoke the base IFS provider's implementation directly even if the layered provider puts its own entry points for these functions into the procedure dispatch table.</li>
<li>The provider cannot rely on any ability to post-process overlapped I/O using 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>, 
<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>, 
<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>, 
<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>, or 
<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>. Post-processing notification may happen through completion ports and bypass the layered provider entirely. A layered provider has no way to determine that a completion port was used or determine what port it is. The layered provider has no way to insert itself into the notification sequence.</li>
<li>The provider should pass through all overlapped I/O requests directly to the base provider using the original overlapped parameters (for example, the 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure and completion routine pointer). The provider should expose the base provider entry point for 
<a href="https://msdn.microsoft.com/8156b8ab-00f8-4325-9b81-3e43053f4f56">WSPGetOverlappedResult</a>. Since some overlapped I/O requests can bypass the layered provider completely, the layered provider cannot reliably mark 
<b>WSAOVERLAPPED</b> structures to determine which ones it can report results for, and which ones would have to be passed through to the underlying provider's 
<b>WSPGetOverlappedResult</b>. This effectively means that 
<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a> has to be a pass-through operation to the underlying provider.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a>



<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a>



<a href="https://msdn.microsoft.com/8156b8ab-00f8-4325-9b81-3e43053f4f56">WSPGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>



<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>



<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>
 

 

