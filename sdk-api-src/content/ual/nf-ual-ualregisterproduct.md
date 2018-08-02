---
UID: NF:ual.UalRegisterProduct
title: UalRegisterProduct function
author: windows-sdk-content
description: Registers a product with User Access Logging (UAL).
old-location: ual\ualregisterproduct.htm
old-project: ual
ms.assetid: EF5A9F0E-DD6A-4CFB-B8A6-AA4298FC6BE8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UalRegisterProduct, UalRegisterProduct function [User Access Logging], ual.ualregisterproduct, ual/UalRegisterProduct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ual.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RECORD_READING_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ualapi.dll
api_name:
 - UalRegisterProduct
product: Windows
targetos: Windows
req.lib: Ualapi.lib
req.dll: Ualapi.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UalRegisterProduct function


## -description


Registers a product with User Access Logging (UAL).


## -parameters




### -param wszProductName [in]

The name of the major product to register with UAL. For example, "Windows Server".


### -param wszRoleName [in]

The name of the role or minor product within the major product to be registered with UAL. For example, "DHCP".


### -param wszGuid

TBD




#### - wszRoleGuid [in]

The GUID associated with the role specified by the <i>wszRoleName</i> parameter.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.



