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

# SHUpdateImageA function


## -description


Notifies the Shell that an image in the system image list has changed.


## -parameters




### -param pszHashItem [in]

Type: <b>LPCTSTR</b>

A pointer to a string value that specifies the fully qualified path of the file that contains the icon. Use the path that is returned in the buffer pointed to by the <i>szIconFile</i> parameter of <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>.


### -param iIndex [in]

Type: <b>int</b>

An integer that specifies the zero-based index of the icon in the file specified by <i>pszHashItem</i>. Use the value that is pointed to by the <i>piIndex</i> parameter of <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>.


### -param uFlags [in]

Type: <b>UINT</b>

An unsigned integer that specifies the flags that determine the icon attributes. Set <i>uFlags</i> to the value that is pointed to by the <i>pwFlags</i> parameter of <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>. The flags that are relevant to <b>SHUpdateImage</b> are <b>GIL_NOTFILENAME</b> and <b>GIL_SIMULATEDOC</b>.


### -param iImageIndex [in]

Type: <b>int</b>

An integer that specifies the index in the system image list of the icon that is being updated.


## -returns



No return value.




## -remarks



If you do not know the index in the system image list of the icon that you want to update, use <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a> with the <i>uFlags</i> parameter set to <b>SHGFI_SYSICONINDEX</b>.

You must use <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> with the parameters of the old icon that needs to be updated, not those of the new icon you want to replace it with.




## -see-also




<a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a>
 

 

