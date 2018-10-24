---
UID: NF:imapi2.IBurnVerification.get_BurnVerificationLevel
title: IBurnVerification::get_BurnVerificationLevel
author: windows-sdk-content
description: Retrieves the current Burn Verification Level.
old-location: imapi\iburnverification_get_burnverificationlevel.htm
tech.root: imapi
ms.assetid: 4be9191a-8f87-4571-a7b6-60d582ec471d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IBurnVerification interface [IMAPI],get_BurnVerificationLevel method, IBurnVerification.get_BurnVerificationLevel, IBurnVerification::get_BurnVerificationLevel, get_BurnVerificationLevel, get_BurnVerificationLevel method [IMAPI], get_BurnVerificationLevel method [IMAPI],IBurnVerification interface, imapi.iburnverification_get_burnverificationlevel, imapi2/IBurnVerification::get_BurnVerificationLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IBurnVerification.get_BurnVerificationLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBurnVerification::get_BurnVerificationLevel


## -description


Retrieves  the current Burn Verification Level.


## -parameters




### -param value

Pointer to an <a href="https://msdn.microsoft.com/83a267b7-8b25-49b8-b1d0-83efbad8fa2a">IMAPI_BURN_VERIFICATION_LEVEL</a> enumeration that specifies the current the Burn Verification Level.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/3a410ab8-dfc3-4c30-a198-3888ed750a6d">IBurnVerification</a>



<a href="https://msdn.microsoft.com/83a267b7-8b25-49b8-b1d0-83efbad8fa2a">IMAPI_BURN_VERIFICATION_LEVEL</a>
 

 

