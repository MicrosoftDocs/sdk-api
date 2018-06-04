---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# FILE_ID_DESCRIPTOR structure


## -description


Specifies the type of ID that is being used.


## -struct-fields




### -field dwSize

The size of this <b>FILE_ID_DESCRIPTOR</b> 
      structure.


### -field Type

The discriminator for the union indicating the type of identifier that is being passed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FileIdType"></a><a id="fileidtype"></a><a id="FILEIDTYPE"></a><dl>
<dt><b>FileIdType</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use the <b>FileId</b> member of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="ObjectIdType"></a><a id="objectidtype"></a><a id="OBJECTIDTYPE"></a><dl>
<dt><b>ObjectIdType</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use the <b>ObjectId</b> member of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="ExtendedFileIdType"></a><a id="extendedfileidtype"></a><a id="EXTENDEDFILEIDTYPE"></a><dl>
<dt><b>ExtendedFileIdType</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Use the <b>ExtendedFileId</b> member of the union.
        

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.FileId

The ID of the file to open.


### -field DUMMYUNIONNAME.ObjectId

The ID of the object to open.


### -field DUMMYUNIONNAME.ExtendedFileId

A <a href="https://msdn.microsoft.com/254ea6a9-e1dd-4b97-91f7-2693065c4bb8">FILE_ID_128</a> structure containing the 128-bit file ID of the file. This is used on ReFS file systems.
       

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This member is not supported before Windows 8 and Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/254ea6a9-e1dd-4b97-91f7-2693065c4bb8">FILE_ID_128</a>



<a href="https://msdn.microsoft.com/7e46ba94-e3cd-4d6c-962f-5d5bd55d45a1">FILE_ID_TYPE</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>



<a href="https://msdn.microsoft.com/caa757a2-fc3f-4883-8d3e-b98d28f92517">OpenFileById</a>
 

 

