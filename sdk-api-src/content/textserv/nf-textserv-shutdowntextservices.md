---
UID: NF:textserv.ShutdownTextServices
title: ShutdownTextServices function
author: windows-sdk-content
description: Disconnects a host from a text services instance.
old-location: controls\shutdowntextservices.htm
tech.root: controls
ms.assetid: 3367D22B-1F9E-4D70-8907-0F218A23AE7E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ShutdownTextServices, ShutdownTextServices function [Windows Controls], controls.shutdowntextservices, textserv/ShutdownTextServices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: textserv.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msftedit.dll
api_name:
 - ShutdownTextServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ShutdownTextServices function


## -description


Disconnects a host from a text services instance. 


## -parameters




### -param pTextServices [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A text services instance created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/Bb787722(v=VS.85).aspx">CreateTextServices</a> function.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the text services object was created successfully, the return value is S_OK. 

If the function fails, one of the following COM error codes are returned. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTextServices</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



A host calls this function when the host is being freed. Calling this function is necessary because all text services instances maintain a host pointer for which the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method has not been called. This function calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method on the text services instance and, if this is not the last reference to the text services object, nulls out the host pointer in the text services object and prepares the control to handle failed operations that require host services. This function allows any other outstanding references to the text services object to work or fail gracefully depending on the service required.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787722(v=VS.85).aspx">CreateTextServices</a>
 

 

