---
UID: NF:mfapi.MFBeginCreateFile
title: MFBeginCreateFile function
author: windows-sdk-content
description: Begins an asynchronous request to create a byte stream from a file.
old-location: mf\mfbegincreatefile.htm
tech.root: medfound
ms.assetid: aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MFBeginCreateFile, MFBeginCreateFile function [Media Foundation], aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd, mf.mfbegincreatefile, mfapi/MFBeginCreateFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFBeginCreateFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFBeginCreateFile function


## -description



Begins an asynchronous request to create a byte stream from a file.




## -parameters




### -param AccessMode [in]

The requested access mode, specified as a member of the <a href="https://msdn.microsoft.com/38108686-5378-4844-8d5a-a433e89f62bb">MF_FILE_ACCESSMODE</a> enumeration.


### -param OpenMode [in]

The behavior of the function if the file already exists or does not exist, specified as a member of the <a href="https://msdn.microsoft.com/0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6">MF_FILE_OPENMODE</a> enumeration.


### -param fFlags [in]

Bitwise <b>OR</b> of values from the <a href="https://msdn.microsoft.com/1e1c906e-c832-4df1-96f5-86e690c3c34e">MF_FILE_FLAGS</a> enumeration.


### -param pwszFilePath [in]

Pointer to a null-terminated string containing the file name.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface


### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


### -param ppCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="https://msdn.microsoft.com/b3c0cad8-d578-4752-a2ea-0aa5c35a181a">MFCancelCreateFile</a> function. The caller must release the interface. This parameter is optional and can be <b>NULL</b>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



When the request is completed, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. The callback object should then call the <a href="https://msdn.microsoft.com/daa92660-5d0d-4c7c-985a-ad621eca4bfc">MFEndCreateFile</a> function to get a pointer to the byte stream.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

