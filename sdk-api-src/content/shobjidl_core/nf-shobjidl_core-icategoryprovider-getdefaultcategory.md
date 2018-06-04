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

# ICategoryProvider::GetDefaultCategory


## -description


Enables the folder to override the default grouping.


## -parameters




### -param pguid [out]

Type: <b>GUID*</b>

Not used.


### -param pscid [out]

Type: <b><a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a>*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no default group.

</td>
</tr>
</table>
 




## -remarks



<b>ICategoryProvider::GetDefaultCategory</b> returns an <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure that is used by the default categorizer. The method returns S_FALSE if a default group is not supported.

<b>ICategoryProvider::GetDefaultCategory</b> is called only when a folder is first opened. After that, the user's grouping choice is cached in the <a href="_inet_IPropertyBag_Interface_cpp">property bag</a> storing the state of the view. To force a call to <b>ICategoryProvider::GetDefaultCategory</b> after the folder is first opened, the <b>Shell</b> and <b>ShellNoRoam</b> registry keys must be deleted. They are found in the following location.

                <pre xml:space="preserve"><b>HKEY_CURRENT_USER</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>Shell</b>
            <b>ShellNoRoam</b></pre>




