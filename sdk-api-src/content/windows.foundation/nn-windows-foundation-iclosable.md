---
UID: NN:windows.foundation.IClosable
title: IClosable (windows.foundation.h)
description: Defines a method to release allocated resources.
helpviewer_keywords: ["IClosable","IClosable interface [Windows Runtime]","IClosable interface [Windows Runtime]","described","windows/IClosable","winrt.iclosable"]
old-location: winrt\iclosable.htm
tech.root: WinRT
ms.assetid: 856C7D91-15AB-4101-BC5F-232004AD6DF4
ms.date: 12/05/2018
ms.keywords: IClosable, IClosable interface [Windows Runtime], IClosable interface [Windows Runtime],described, windows/IClosable, winrt.iclosable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IClosable
 - windows.foundation/IClosable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IClosable
---

# IClosable interface


## -description

Defines a method to release allocated resources.

## -inheritance

The <b>IClosable</b> interface inherits from the <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface. <b>IClosable</b> also has these types of members:

## -remarks

Use the <b>IClosable</b> interface to manage the lifetime of system resources, like file handles and network sockets, that are used by a Windows Runtime object. 

Some system resources are used exclusively by a single piece of code and must be freed before other code can use them. For example, opening a file for read/write access prevents other code from opening the same file for read/write access, so the code that opened the file must close the file handle before other code can open it.

 Other system resources aren't exclusive-use. Many hardware devices, like sensors, geolocation, SMS, and portable devices can be opened multiple times within the same app or by multiple apps.

The <b>IClosable</b> interface enables managing exclusive-use system resources.   When you call the <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> method on a Windows Runtime object, the object releases its system resources so that they're available for other code to use. Objects that use only shared system resources, like memory and shareable devices, don't implement <b>IClosable</b>.

When you implement the <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> method in a Windows Runtime object, your  code must release all of the exclusive-use resources that it holds. If the object has references to other closeable Windows Runtime objects, it must call <b>Close</b> on the objects before they're released. Also, your code must release other resources, like references to other Windows Runtime and Component Object Model (COM) objects, and    non-exclusive system resources like memory buffers.

Calling the <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> method on an object leaves the object in memory, but the object no longer has the system resources that it needs to function properly. Members that depend on released system resources must return <b>RO_E_CLOSED</b> to indicate that the object is closed and that these members no longer work.

Methods defined by the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interfaces must continue to function normally after <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> has been called.

Calling <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> on an object that is already closed has no effect and returns <b>S_OK</b>. 

Usually, your objects track their closed state by setting a boolean flag when Close is called, or by checking held resources for null or another sentinel value.

Objects don't need to synchronize access to the <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> method. This means that race conditions are possible in which one thread calls <b>Close</b> on an object while another thread is using the object. In this case, it's possible to get an error other than <b>RO_E_CLOSED</b>, but you must ensure that the object doesn't cause an access violation.

The <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> method doesn't block while waiting for asynchronous operations to complete. So the underlying system resources might not be completely released when the <b>Close</b> method returns. To ensure deterministic closing, the caller must wait for all asynchronous operations to complete or cancel. Objects must complete releasing their system resources as quickly as possible in the face of outstanding asynchronous operations, but must not block while waiting for these to complete.


If your closeable Windows Runtime object exposes an exclusive-use resource to other objects, it must provide a way to affect the ownership semantics of any closeable objects that it holds.  For example, the <a href="/uwp/api/windows.storage.streams.idatareader">DataReader</a> class provides a <a href="/uwp/api/windows.storage.streams.idatareader.detachstream">DetachStream</a> method that returns the <a href="/previous-versions/hh438387(v=vs.85)">IInputStream</a> that it received when it was created. When <b>DetachStream</b> is called, the <b>DataReader</b> is no longer the owner of the  <b>IInputStream</b>, so the <b>DataReader</b> doesn't call <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-iclosable-close">Close</a> on the <b>IInputStream</b>.
