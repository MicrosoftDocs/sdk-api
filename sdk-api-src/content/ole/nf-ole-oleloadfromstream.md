---
UID: NF:ole.OleLoadFromStream
title: OleLoadFromStream function
author: windows-sdk-content
description: Loads an object from the stream.
old-location: com\oleloadfromstream.htm
tech.root: com
ms.assetid: 2d54a0ef-906b-4886-a095-4ff2f3d4e634
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OleLoadFromStream, OleLoadFromStream function [COM], _ole_OleLoadFromStream, com.oleloadfromstream, ole/OleLoadFromStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole.h
req.include-header: Ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
 - OleLoadFromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleLoadFromStream function


## -description


Loads an object from the stream.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD


### -param arg4

TBD


### -param arg5

TBD


### -param arg6

TBD




#### - [in]

Pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface on the stream from which the object is to be loaded.


#### - iidInterface [in]

Interface identifier (IID) the caller wants to use to communicate with the object after it is loaded.


#### - ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly loaded object.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
</table>
 

This function can also return any of the error values returned by the <a href="https://msdn.microsoft.com/bcf11c5b-e164-4a0f-b30f-ee9e76c4356d">ReadClassStm</a> and <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> functions, and the <a href="https://msdn.microsoft.com/351e1187-9959-4542-8778-925457c3b8e3">IPersistStream::Load</a> method.




## -remarks



<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data. For more information, see <a href="http://go.microsoft.com/fwlink/?LinkId=798821">Untrusted Data Security Risks</a>.

</div>
<div> </div>
This function can be used to load an object that supports the <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> interface. The CLSID of the object must immediately precede the object's data in the stream, which is accomplished by the companion function <a href="https://msdn.microsoft.com/0085c6a8-1a94-4379-9937-c8d792d130da">OleSaveToStream</a> (or the operations it wraps, which are described under that topic).



If the CLSID for the stream is CLSID_NULL, the <i>ppvObj</i> parameter is set to <b>NULL</b>.





## -see-also




<a href="https://msdn.microsoft.com/0085c6a8-1a94-4379-9937-c8d792d130da">OleSaveToStream</a>
 

 

