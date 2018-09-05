---
UID: NF:mergemod.IMsmMerge.OpenDatabase
title: IMsmMerge::OpenDatabase
author: windows-sdk-content
description: The OpenDatabase method opens a Windows Installer installation database, located at a specified path, that is to be merged with a module. For more information, see the OpenDatabase method of the Merge object.
old-location: setup\imsmmerge_opendatabase.htm
old-project: msi
ms.assetid: cafe02a0-2e86-43f6-9cde-e3dd23bdfc4c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMsmMerge interface,OpenDatabase method, IMsmMerge.OpenDatabase, IMsmMerge::OpenDatabase, OpenDatabase, OpenDatabase method, OpenDatabase method,IMsmMerge interface, _msi_opendatabase_function, mergemod/IMsmMerge::OpenDatabase, setup.imsmmerge_opendatabase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.OpenDatabase
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmMerge::OpenDatabase


## -description


The 
<b>OpenDatabase</b> method opens a Windows Installer installation database, located at a specified path, that is to be merged with a module. For more information, see the 
<a href="https://msdn.microsoft.com/86f168e5-bc76-476d-9757-9b2a21bb9c4b">OpenDatabase</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. 

<b>IMsmMerge2::OpenDatabase</b>    Mergemod.dll version 2.0 and later.<div> </div><b>IMsmMerge::OpenDatabase</b>      All Mergemod.dll versions.
			
			


## -parameters




### -param Path

Path to the database being opened.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error opening the database.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

