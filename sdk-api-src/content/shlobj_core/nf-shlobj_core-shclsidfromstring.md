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

# SHCLSIDFromString function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="https://msdn.microsoft.com/36cc9037-480f-491f-a9bb-5aa1e707781e">CLSIDFromString</a> instead.]

Takes the string form of a class identifier (CLSID) and creates the corresponding CLSID.


## -parameters




### -param psz [in]

Type: <b>PCWSTR</b>

A Unicode string that contains the CLSID in the format, <code>{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</code>.


### -param pclsid

TBD




#### - pcClsid [out]

Type: <b>CLSID*</b>

A pointer to a CLSID value that, when this function returns successfully, receives the converted string as a CLSID.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



