---
UID: NF:casetup.ICertSrvSetup.IsPropertyEditable
title: ICertSrvSetup::IsPropertyEditable (casetup.h)
author: windows-sdk-content
description: Indicates to the caller whether a specified property can be edited.
old-location: security\icertsrvsetup_ispropertyeditable.htm
tech.root: SecCrypto
ms.assetid: 2facae59-aa96-4ac7-97e1-ff094022681a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],IsPropertyEditable method, ICertSrvSetup.IsPropertyEditable, ICertSrvSetup::IsPropertyEditable, IsPropertyEditable, IsPropertyEditable method [Security], IsPropertyEditable method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::IsPropertyEditable, security.icertsrvsetup_ispropertyeditable
ms.topic: method
f1_keywords: 
 - "casetup/ICertSrvSetup.IsPropertyEditable"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertSrvSetup::IsPropertyEditable


## -description


The <b>IsPropertyEditable</b> method indicates to the caller whether a specified property can be edited.


## -parameters




### -param propertyId [in]

A <a href="https://docs.microsoft.com/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a> constant that specifies the type of property to query.


### -param pbEditable [out]

A value that indicates whether the property can be edited.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>
 

 

