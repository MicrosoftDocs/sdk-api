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

# IFsrmClassificationManager::ClearFileProperty


## -description


Attempts to remove the specified property from the file or folder.

<b>Windows Server 2008 R2:  </b>Only files are supported until Windows Server 2012.


## -parameters




### -param filePath [in]

The file that contains the property that you want to remove. You must specify an absolute path to the file. 
      You cannot specify a file share.


### -param property






#### - propertyName [in]

The name of the property to remove from the file.


## -returns



The method returns the following return values.




## -remarks



The property is removed from the file if the storage module is able to remove the property; otherwise, the 
     property's value is cleared using the values in the following list.

<table>
<tr>
<th>Property type</th>
<th>Cleared value</th>
</tr>
<tr>
<td>Boolean</td>
<td></td>
</tr>
<tr>
<td>Date</td>
<td></td>
</tr>
<tr>
<td>Hierarchy</td>
<td></td>
</tr>
<tr>
<td>Integer</td>
<td></td>
</tr>
<tr>
<td>Multiple choice list</td>
<td></td>
</tr>
<tr>
<td>Single choice list</td>
<td></td>
</tr>
<tr>
<td>Multi-string</td>
<td></td>
</tr>
<tr>
<td>Ordered list</td>
<td></td>
</tr>
<tr>
<td>String</td>
<td>Empty string</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7">IFsrmClassificationManager::GetFileProperty</a>



<a href="https://msdn.microsoft.com/0f13f00e-6ca2-4436-822e-01eff638c446">IFsrmClassificationManager::SetFileProperty</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

