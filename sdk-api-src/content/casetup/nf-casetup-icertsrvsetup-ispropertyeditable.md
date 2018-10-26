---
UID: NF:casetup.ICertSrvSetup.IsPropertyEditable
title: ICertSrvSetup::IsPropertyEditable
author: windows-sdk-content
description: Indicates to the caller whether a specified property can be edited.
old-location: security\icertsrvsetup_ispropertyeditable.htm
tech.root: seccrypto
ms.assetid: 2facae59-aa96-4ac7-97e1-ff094022681a
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ICertSrvSetup interface [Security],IsPropertyEditable method, ICertSrvSetup.IsPropertyEditable, ICertSrvSetup::IsPropertyEditable, IsPropertyEditable, IsPropertyEditable method [Security], IsPropertyEditable method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::IsPropertyEditable, security.icertsrvsetup_ispropertyeditable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.IsPropertyEditable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::IsPropertyEditable


## -description


The <b>IsPropertyEditable</b> method indicates to the caller whether a specified property can be edited.


## -parameters




### -param propertyId [in]

A <a href="https://msdn.microsoft.com/en-us/library/Bb648668(v=VS.85).aspx">CASetupProperty</a> constant that specifies the type of property to query.


### -param pbEditable [out]

A value that indicates whether the property can be edited.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736371(v=VS.85).aspx">ICertSrvSetup</a>
 

 

