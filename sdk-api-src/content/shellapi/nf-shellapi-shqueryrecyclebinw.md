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

# SHQueryRecycleBinW function


## -description


Retrieves the size of the Recycle Bin and the number of items in it, for a specified drive.


## -parameters




### -param pszRootPath [in, optional]

Type: <b>LPCTSTR</b>

The address of a <b>null</b>-terminated string of maximum length MAX_PATH to contain the path of the root drive on which the Recycle Bin is located. This parameter can contain the address of a string formatted with the drive, folder, and subfolder names (C:\Windows\System...).


### -param pSHQueryRBInfo [in, out]

Type: <b>LPSHQUERYRBINFO</b>

The address of a <a href="https://msdn.microsoft.com/7e9bc7e9-5712-45e7-a424-0afb62f26450">SHQUERYRBINFO</a> structure that receives the Recycle Bin information. The <b>cbSize</b> member of the structure must be set to the size of the structure before calling this API.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



With Windows 2000, if <b>NULL</b> is passed in the <i>pszRootPath</i> parameter, the function fails and returns an E_INVALIDARG error code. In earlier versions of the operating system, you can pass an empty string or <b>NULL</b>. If <i>pszRootPath</i> contains an empty string or <b>NULL</b>, information is retrieved for all Recycle Bins on all drives.




## -see-also




<a href="https://msdn.microsoft.com/c3995be7-bc8b-4e1f-8ef6-fdf4c0a75720">SHEmptyRecycleBin</a>
 

 

