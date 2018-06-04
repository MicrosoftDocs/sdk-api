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

# CryptUIDlgCertMgr function


## -description


The <b>CryptUIDlgCertMgr</b> function displays a dialog box that allows the user to manage certificates.


## -parameters




### -param pCryptUICertMgr [in]

A pointer to a <a href="https://msdn.microsoft.com/e6c24d16-0ae2-443c-8971-2d7da3aae963">CRYPTUI_CERT_MGR_STRUCT</a> structure that contains information about how to create the dialog box.


## -returns



The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE.</b>



