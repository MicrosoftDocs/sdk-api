---
UID: NF:imapi2.IBurnVerification.put_BurnVerificationLevel
title: IBurnVerification::put_BurnVerificationLevel
author: windows-driver-content
description: Sets the Burn Verification Level.
old-location: imapi\iburnverification_put_burnverificationlevel.htm
old-project: imapi
ms.assetid: 71842038-91dc-4de5-8169-3bc97ef288c6
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IBurnVerification interface [IMAPI],put_BurnVerificationLevel method, IBurnVerification.put_BurnVerificationLevel, IBurnVerification::put_BurnVerificationLevel, imapi.iburnverification_put_burnverificationlevel, imapi2/IBurnVerification::put_BurnVerificationLevel, put_BurnVerificationLevel, put_BurnVerificationLevel method [IMAPI], put_BurnVerificationLevel method [IMAPI],IBurnVerification interface
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IBurnVerification.put_BurnVerificationLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IBurnVerification::put_BurnVerificationLevel


## -description


Sets the   Burn Verification Level.


## -parameters




### -param value

Value that defines the Burn Verification Level. For possible values, see <a href="https://msdn.microsoft.com/83a267b7-8b25-49b8-b1d0-83efbad8fa2a">IMAPI_BURN_VERIFICATION_LEVEL</a>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/3a410ab8-dfc3-4c30-a198-3888ed750a6d">IBurnVerification</a>



<a href="https://msdn.microsoft.com/83a267b7-8b25-49b8-b1d0-83efbad8fa2a">IMAPI_BURN_VERIFICATION_LEVEL</a>
 

 

