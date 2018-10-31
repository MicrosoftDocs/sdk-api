---
UID: NF:certpoleng.PstGetTrustAnchors
title: PstGetTrustAnchors function
author: windows-sdk-content
description: Retrieves a list of certification authorities (CAs) trusted by the specified server.
old-location: security\pstgettrustanchors.htm
tech.root: secauthn
ms.assetid: bbd69763-6801-4321-be18-802d48850d8c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PstGetTrustAnchors, PstGetTrustAnchors function [Security], certpoleng/PstGetTrustAnchors, security.pstgettrustanchors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: certpoleng.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certpoleng.lib
req.dll: Certpoleng.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certpoleng.dll
api_name:
 - PstGetTrustAnchors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PstGetTrustAnchors function


## -description


Retrieves a list of <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authorities</a> (CAs) trusted by the specified server.


## -parameters




### -param pTargetName [in]

The name of the server to check.


### -param cCriteria [in]

The number of elements in the <i>rgpCriteria</i> array.


### -param rgpCriteria [in, optional]

A constant pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Dd433801(v=VS.85).aspx">CERT_SELECT_CRITERIA</a> structures that specify the criteria used to select certificate chains.


### -param ppTrustedIssuers [out]

A pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Aa380078(v=VS.85).aspx">SecPkgContext_IssuerListInfoEx</a> structures that receive the CAs trusted by the server specified by the <i>pTargetName</i> parameter.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.



