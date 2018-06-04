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

# ICDBurn::Burn


## -description


Instructs data to be copied from the staging area to a writable CD.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the UI.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>staging area</i> has a default location of %userprofile%\Local Settings\Application Data\Microsoft\CD Burning. Its actual path can be retrieved through <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a>, <a href="https://msdn.microsoft.com/4c39fdc1-5e43-4042-8703-fb72c88e2637">SHGetSpecialFolderPath</a>, <a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>, <a href="https://msdn.microsoft.com/10b00497-fc3b-4e34-acd8-bc0721c0dc05">SHGetSpecialFolderLocation</a>, or <a href="https://msdn.microsoft.com/7e92e136-1036-4c96-931f-6e0129fb839a">SHGetFolderPathAndSubDir</a> by using the CSIDL_CDBURN_AREA value.



