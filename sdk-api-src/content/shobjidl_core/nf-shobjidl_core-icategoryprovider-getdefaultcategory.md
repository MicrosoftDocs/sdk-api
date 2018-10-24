---
UID: NF:shobjidl_core.ICategoryProvider.GetDefaultCategory
title: ICategoryProvider::GetDefaultCategory
author: windows-sdk-content
description: Enables the folder to override the default grouping.
old-location: shell\ICategoryProvider_GetDefaultCategory.htm
tech.root: shell
ms.assetid: b5a5d04c-b666-4063-bf0b-02564aa967ab
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetDefaultCategory, GetDefaultCategory method [Windows Shell], GetDefaultCategory method [Windows Shell],ICategoryProvider interface, ICategoryProvider interface [Windows Shell],GetDefaultCategory method, ICategoryProvider.GetDefaultCategory, ICategoryProvider::GetDefaultCategory, inet_ICategoryProvider_GetDefaultCategory, shell.ICategoryProvider_GetDefaultCategory, shobjidl_core/ICategoryProvider::GetDefaultCategory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICategoryProvider.GetDefaultCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




