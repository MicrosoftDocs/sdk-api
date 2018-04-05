---
UID: NF:encdec.IETFilterConfig.GetSecureChannelObject
title: IETFilterConfig::GetSecureChannelObject method
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\ietfilterconfig_getsecurechannelobject.htm
old-project: mstv
ms.assetid: 385f4525-97b0-4973-8b74-a05816e43556
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetSecureChannelObject method [Microsoft TV Technologies], GetSecureChannelObject method [Microsoft TV Technologies], IETFilterConfig interface, GetSecureChannelObject,IETFilterConfig.GetSecureChannelObject, IETFilterConfig, IETFilterConfig interface [Microsoft TV Technologies], GetSecureChannelObject method, IETFilterConfig::GetSecureChannelObject, IETFilterConfigGetSecureChannelObject, encdec/IETFilterConfig::GetSecureChannelObject, mstv.ietfilterconfig_getsecurechannelobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IETFilterConfig.GetSecureChannelObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IETFilterConfig::GetSecureChannelObject method


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>GetSecureChannelObject</b> method retrieves the secure channel object used to encrypt the stream.


## -parameters




### -param ppUnkDRMSecureChannel [out]

Receives a pointer to the secure channel object's <b>IUnknown</b> interface.


## -returns



Returns an <b>HRESULT</b>.




## -remarks




        If the method succeeds, the caller must release the <b>IUnknown</b> interface.
      




## -see-also




<a href="https://msdn.microsoft.com/6fa3da1b-863b-4ed7-b5ef-4ed1c05d2456">IETFilterConfig Interface</a>
 

 

