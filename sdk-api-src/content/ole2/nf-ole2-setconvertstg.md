---
UID: NF:ole2.SetConvertStg
title: SetConvertStg function
author: windows-sdk-content
description: The SetConvertStg function sets the convert bit in a storage object to indicate that the object is to be converted to a new class when it is opened. The setting can be retrieved with a call to the GetConvertStg function.
old-location: stg\setconvertstg.htm
tech.root: Stg
ms.assetid: 98c8fd20-6384-4656-941c-1f24d9a4d4a9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetConvertStg, SetConvertStg function [Structured Storage], _stg_setconvertstg, ole2/SetConvertStg, stg.setconvertstg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
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
api_name:
 - SetConvertStg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetConvertStg function


## -description


The 
<b>SetConvertStg</b> function sets the convert bit in a storage object to indicate that the object is to be converted to a new class when it is opened. The setting can be retrieved with a call to the 
<a href="https://msdn.microsoft.com/748649a2-cf75-4ffa-ac1f-4a148b845d21">GetConvertStg</a> function.


## -parameters




### -param pStg


<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the storage object in which to set the conversion bit.


### -param fConvert

If <b>TRUE</b>, sets the conversion bit for the object to indicate the object is to be converted when opened. If <b>FALSE</b>, clears the conversion bit.


## -returns



See the 
<a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">IStorage::CreateStream</a>, 
<a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">IStorage::OpenStream</a>, 
<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a>, and 
<a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> methods for possible storage and stream access errors.




## -remarks



The 
<b>SetConvertStg</b> function determines the status of the convert bit in a contained object. It is called by both the container application and the server in the process of converting an object from one class to another. When a user specifies through a <b>Convert To</b> dialog (which the container produces with a call to the 
<a href="https://msdn.microsoft.com/en-us/library/ms680694(v=VS.85).aspx">OleUIConvert</a> function) that an object is to be converted, the container must take the following steps:

<ol>
<li>Unload the object if it is currently loaded.</li>
<li>Call 
<a href="https://msdn.microsoft.com/5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e">WriteClassStg</a> to write the new CLSID to the object storage.</li>
<li>Call 
<a href="https://msdn.microsoft.com/ef60493c-164e-4633-a248-05c4afade937">WriteFmtUserTypeStg</a> to write the new user-type name and the existing main format to the storage.</li>
<li>Call 
<b>SetConvertStg</b> with the <i>fConvert</i> parameter set to <b>TRUE</b> to indicate that the object has been tagged for conversion to a new class the next time it is loaded.</li>
<li>Just before the object is loaded, call 
<a href="https://msdn.microsoft.com/en-us/library/ms695230(v=VS.85).aspx">OleDoAutoConvert</a> to handle any needed object conversion, unless you call 
<a href="https://msdn.microsoft.com/en-us/library/ms694338(v=VS.85).aspx">OleLoad</a>, which calls it internally.</li>
</ol>
When an object is initialized from a storage object and the server is the destination of a convert-to operation, the object server should do the following:

<ol>
<li>Call the 
<a href="https://msdn.microsoft.com/748649a2-cf75-4ffa-ac1f-4a148b845d21">GetConvertStg</a> function to retrieve the value of the conversion bit.</li>
<li>If the bit is set, the server reads the data out of the object according to the format associated with the new CLSID.</li>
<li>When the object is asked to save itself, the object should call the 
<a href="https://msdn.microsoft.com/ef60493c-164e-4633-a248-05c4afade937">WriteFmtUserTypeStg</a> function using the normal native format and user type of the object.</li>
<li>The object should then call 
<b>SetConvertStg</b> with the <i>fConvert</i> parameter set to <b>FALSE</b> to reset the object's conversion bit.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/748649a2-cf75-4ffa-ac1f-4a148b845d21">GetConvertStg</a>
 

 

