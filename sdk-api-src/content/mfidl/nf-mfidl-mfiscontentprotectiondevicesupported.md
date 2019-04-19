---
UID: NF:mfidl.MFIsContentProtectionDeviceSupported
title: MFIsContentProtectionDeviceSupported function (mfidl.h)
author: windows-sdk-content
description: Checks whether a hardware security processor is supported for the specified media protection system.
old-location: mf\mfiscontentprotectiondevicesupported.htm
tech.root: medfound
ms.assetid: 8C91C204-49C0-41CF-A9E1-F9C53388604A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFIsContentProtectionDeviceSupported, MFIsContentProtectionDeviceSupported function [Media Foundation], mf.mfiscontentprotectiondevicesupported, mfidl/MFIsContentProtectionDeviceSupported
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFIsContentProtectionDeviceSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFIsContentProtectionDeviceSupported function


## -description


Checks whether a hardware security processor is supported for the specified media protection system.


## -parameters




### -param ProtectionSystemId [in]

The identifier of the protection system that you want to check.


### -param isSupported [out]

<b>TRUE</b> if the hardware security processor is supported for the specified protection system; otherwise <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

