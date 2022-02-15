---
UID: NE:inspectable.TrustLevel
title: TrustLevel (inspectable.h)
description: Represents the trust level of an activatable class.
helpviewer_keywords: ["BaseTrust","FullTrust","PartialTrust","RegisteredTrustLevel","TrustLevel","TrustLevel enumeration [Windows Runtime]","inspectable/BaseTrust","inspectable/FullTrust","inspectable/PartialTrust","inspectable/TrustLevel","winrt.trustlevel"]
old-location: winrt\trustlevel.htm
tech.root: WinRT
ms.assetid: 75E30E4B-EE5F-41C4-AC22-91D542E920EB
ms.date: 12/05/2018
ms.keywords: BaseTrust, FullTrust, PartialTrust, RegisteredTrustLevel, TrustLevel, TrustLevel enumeration [Windows Runtime], inspectable/BaseTrust, inspectable/FullTrust, inspectable/PartialTrust, inspectable/TrustLevel, winrt.trustlevel
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TrustLevel
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TrustLevel
 - inspectable/TrustLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Inspectable.h
api_name:
 - TrustLevel
---

# TrustLevel enumeration


## -description

Represents the trust level of an activatable class.

## -enum-fields

### -field BaseTrust:0

The component has access to resources that are not protected.

### -field PartialTrust

The component has access to resources requested in the app manifest and approved by the user.

### -field FullTrust

The component requires the full privileges of the user.

## -remarks

Classes can be activated depending on the trust level of the caller and the trust classification of the activatable class.


<a href="/previous-versions/dn408470(v=vs.85)">RegisteredTrustLevel</a> is an alias for this enumeration.

## -see-also

<a href="/windows/desktop/api/inspectable/nf-inspectable-iinspectable-gettrustlevel">IInspectable::GetTrustLevel</a>
