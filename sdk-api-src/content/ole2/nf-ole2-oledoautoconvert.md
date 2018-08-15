---
UID: NF:ole2.OleDoAutoConvert
title: OleDoAutoConvert function
author: windows-sdk-content
description: Automatically converts an object to a new class if automatic conversion for that object class is set in the registry.
old-location: com\oledoautoconvert.htm
old-project: com
ms.assetid: fe470f8a-b2f0-48a4-a270-77420bd1472a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OleDoAutoConvert, OleDoAutoConvert function [COM], _com_OleDoAutoConvert, com.oledoautoconvert, ole2/OleDoAutoConvert
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleDoAutoConvert
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleDoAutoConvert function


## -description


Automatically converts an object to a new class if automatic conversion for that object class is set in the registry.


## -parameters




### -param pStg [in]

A pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object to be converted.


### -param pClsidNew [out]

A pointer to the new CLSID for the object being converted. If there was no automatic conversion, this may be the same as the original class.


## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
No conversion is needed or a conversion was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_KEYMISSING</b></dt>
</dl>
</td>
<td width="60%">
The function cannot read a key from the registry.

</td>
</tr>
</table>
 

This function can also return any of the error values returned by the <a href="https://msdn.microsoft.com/f84e578a-d2ed-4b7b-9b7c-5d63f12d5781">OleGetAutoConvert</a> function. When accessing storage and stream objects, see the <a href="https://msdn.microsoft.com/f1f0564e-0ecd-4b73-8863-9d6b6746fd02">IStorage::OpenStorage</a> and <a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">IStorage::OpenStream</a> methods for possible errors. When it is not possible to determine the existing CLSID or when it is not possible to update the storage object with new information, see the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface for other error return values.




## -remarks



<b>OleDoAutoConvert</b> automatically converts an object if automatic conversion has previously been specified in the registry by the <a href="https://msdn.microsoft.com/39abf385-962a-4b20-b319-501c8130e050">OleSetAutoConvert</a> function. Object conversion means that the object is permanently associated with a new CLSID. Automatic conversion is typically specified by the setup program for a new version of an object application, so that objects created by its older versions can be automatically updated.

The storage object must be in the unloaded state when <b>OleDoAutoConvert</b> is called.

A container application that supports object conversion should call <b>OleDoAutoConvert</b> each time it loads an object. If the container uses the <a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a> helper function, it need not call <b>OleDoAutoConvert</b> explicitly because <b>OleLoad</b> calls it internally.

<b>OleDoAutoConvert</b> first determines whether any conversion is required by calling the <a href="https://msdn.microsoft.com/f84e578a-d2ed-4b7b-9b7c-5d63f12d5781">OleGetAutoConvert</a> function, which, if no conversion is required, returns S_OK. If the object requires conversion, <b>OleDoAutoConvert</b> modifies and converts the storage object by activating the new object application. The new object application reads the existing data format, but saves the object in the new native format for the object application.

If the object to be automatically converted is an OLE 1 object, the ItemName string is stored in a stream called "\1Ole10ItemName." If this stream does not exist, the object's item name is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/f84e578a-d2ed-4b7b-9b7c-5d63f12d5781">OleGetAutoConvert</a>



<a href="https://msdn.microsoft.com/39abf385-962a-4b20-b319-501c8130e050">OleSetAutoConvert</a>
 

 

