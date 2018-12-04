---
UID: NF:coml2api.GetConvertStg
title: GetConvertStg function
author: windows-sdk-content
description: The GetConvertStg function returns the current value of the convert bit for the specified storage object.
old-location: stg\getconvertstg.htm
tech.root: stg
ms.assetid: 748649a2-cf75-4ffa-ac1f-4a148b845d21
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetConvertStg, GetConvertStg function [Structured Storage], _stg_getconvertstg, coml2api/GetConvertStg, stg.getconvertstg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - GetConvertStg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetConvertStg function


## -description


The 
<b>GetConvertStg</b> function returns the current value of the convert bit for the specified storage object.


## -parameters




### -param pStg [in]


<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the storage object from which the convert bit is to be retrieved.


## -returns




<a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">IStorage::OpenStream</a>, 
<a href="https://msdn.microsoft.com/f1f0564e-0ecd-4b73-8863-9d6b6746fd02">IStorage::OpenStorage</a>, and 
<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> storage and stream access errors.




## -remarks



The 
<b>GetConvertStg</b> function is called by object servers that support the conversion of an object from one format to another. The server must be able to read the storage object using the format of its previous class identifier (CLSID) and write the object using the format of its new CLSID to support the object's conversion. For example, a spreadsheet created by one application can be converted to the format used by a different application.

The convert bit is set by a call to the 
<a href="https://msdn.microsoft.com/98c8fd20-6384-4656-941c-1f24d9a4d4a9">SetConvertStg</a> function. A container application can call this function on the request of an end user, or a setup program can call it when installing a new version of an application. An end user requests converting an object through the <b>Convert To</b> dialog box. When an object is converted, the new CLSID is permanently assigned to the object, so the object is subsequently associated with the new CLSID.

Then, when the object is activated, its server calls the 
<b>GetConvertStg</b> function to retrieve the value of the convert bit from the storage object. If the bit is set, the object's CLSID has been changed, and the server must read the old format and write the new format for the storage object.

After retrieving the bit value, the object application should clear the convert bit by calling the 
<a href="https://msdn.microsoft.com/98c8fd20-6384-4656-941c-1f24d9a4d4a9">SetConvertStg</a> function with its <i>fConvert</i> parameter set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/98c8fd20-6384-4656-941c-1f24d9a4d4a9">SetConvertStg</a>
 

 

