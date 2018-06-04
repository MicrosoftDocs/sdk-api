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

# ICDBurn::GetRecorderDriveLetter


## -description


Gets the drive letter of a CD drive that has been marked as write-enabled.


## -parameters




### -param pszDrive [out]

Type: <b>LPWSTR</b>

A pointer to a string containing the drive letter, for example "F:\".


### -param cch [in]

Type: <b>UINT</b>

The size of the string, in characters, pointed to by pszDrive. This value will normally be 4. Values larger than 4 are allowed, but the extra characters will be ignored by this method. Values less than 4 will generate an E_INVALIDARG error.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




			The drive whose letter designation is returned by this method is the drive that has the <b>Enable cd writing on this drive</b> option selected. This option is found on the drive's property sheet. Only one drive on a system can have this option selected.
			


			If a recordable CD drive is present but that option has been deselected, the method will return an error code.
			



