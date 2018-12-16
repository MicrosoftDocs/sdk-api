---
UID: NF:richole.IRichEditOleCallback.GetNewStorage
title: IRichEditOleCallback::GetNewStorage
author: windows-sdk-content
description: Provides storage for a new object pasted from the clipboard or read in from an Rich Text Format (RTF) stream.
old-location: controls\IRichEditOleCallback_GetNewStorage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetnewstorage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNewStorage, GetNewStorage method [Windows Controls], GetNewStorage method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetNewStorage method, IRichEditOleCallback.GetNewStorage, IRichEditOleCallback::GetNewStorage, _win32_IRichEditOleCallback_GetNewStorage, _win32_IRichEditOleCallback_GetNewStorage_cpp, controls.IRichEditOleCallback_GetNewStorage, controls._win32_IRichEditOleCallback_GetNewStorage, richole/IRichEditOleCallback::GetNewStorage
ms.topic: method
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.GetNewStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOleCallback::GetNewStorage


## -description


Provides storage for a new object pasted from the clipboard or read in from an Rich Text Format (RTF) stream.


## -parameters




### -param lplpstg

Type: <b>LPSTORAGE*</b>

The address of the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface created for the new object. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can return one of the following values.

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
There was an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to do the operation.

</td>
</tr>
</table>
 




## -remarks



This method must be implemented to allow cut, copy, paste, drag, and drop operations of Component Object Model (COM) objects.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774308(v=VS.85).aspx">IRichEditOleCallback</a>



<b>Reference</b>
 

 

