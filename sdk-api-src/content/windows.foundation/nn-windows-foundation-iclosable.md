---
UID: NN:windows.foundation.IClosable
title: IClosable
author: windows-sdk-content
description: Defines a method to release allocated resources.
old-location: winrt\iclosable.htm
tech.root: WinRT
ms.assetid: 856C7D91-15AB-4101-BC5F-232004AD6DF4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IClosable, IClosable interface [Windows Runtime], IClosable interface [Windows Runtime],described, windows/IClosable, winrt.iclosable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
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
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IClosable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IClosable interface


## -description


Defines a method to release allocated resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClosable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IClosable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClosable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a>
</td>
<td align="left" width="63%">
Performs application-defined tasks associated with freeing, releasing, or resetting allocated resources.

</td>
</tr>
</table> 


## -remarks



Use the <b>IClosable</b> interface to manage the lifetime of system resources, like file handles and network sockets, that are used by a Windows Runtime object. 

Some system resources are used exclusively by a single piece of code and must be freed before other code can use them. For example, opening a file for read/write access prevents other code from opening the same file for read/write access, so the code that opened the file must close the file handle before other code can open it.

 Other system resources aren't exclusive-use. Many hardware devices, like sensors, geolocation, SMS, and portable devices can be opened multiple times within the same app or by multiple apps.

The <b>IClosable</b> interface enables managing exclusive-use system resources.   When you call the <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> method on a Windows Runtime object, the object releases its system resources so that they're available for other code to use. Objects that use only shared system resources, like memory and shareable devices, don't implement <b>IClosable</b>.

When you implement the <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> method in a Windows Runtime object, your  code must release all of the exclusive-use resources that it holds. If the object has references to other closeable Windows Runtime objects, it must call <b>Close</b> on the objects before they're released. Also, your code must release other resources, like references to other Windows Runtime and Component Object Model (COM) objects, and    non-exclusive system resources like memory buffers.

Calling the <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> method on an object leaves the object in memory, but the object no longer has the system resources that it needs to function properly. Members that depend on released system resources must return <b>RO_E_CLOSED</b> to indicate that the object is closed and that these members no longer work.

Methods defined by the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interfaces must continue to function normally after <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> has been called.

Calling <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> on an object that is already closed has no effect and returns <b>S_OK</b>. 

Usually, your objects track their closed state by setting a boolean flag when Close is called, or by checking held resources for null or another sentinel value.

Objects don't need to synchronize access to the <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> method. This means that race conditions are possible in which one thread calls <b>Close</b> on an object while another thread is using the object. In this case, it's possible to get an error other than <b>RO_E_CLOSED</b>, but you must ensure that the object doesn't cause an access violation.

The <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> method doesn't block while waiting for asynchronous operations to complete. So the underlying system resources might not be completely released when the <b>Close</b> method returns. To ensure deterministic closing, the caller must wait for all asynchronous operations to complete or cancel. Objects must complete releasing their system resources as quickly as possible in the face of outstanding asynchronous operations, but must not block while waiting for these to complete.


If your closeable Windows Runtime object exposes an exclusive-use resource to other objects, it must provide a way to affect the ownership semantics of any closeable objects that it holds.  For example, the <a href="https://msdn.microsoft.com/562904a7-f881-4054-97d1-2be83f795f89">DataReader</a> class provides a <a href="https://msdn.microsoft.com/de9f9c28-5719-4cd8-95d0-6eb806d311ed">DetachStream</a> method that returns the <a href="https://msdn.microsoft.com/44519D2C-F6C1-4E20-8C84-3C538E1A4BEE">IInputStream</a> that it received when it was created. When <b>DetachStream</b> is called, the <b>DataReader</b> is no longer the owner of the  <b>IInputStream</b>, so the <b>DataReader</b> doesn't call <a href="https://msdn.microsoft.com/B08161D3-01D9-4782-A3FA-EAD15DA8B7D9">Close</a> on the <b>IInputStream</b>.



