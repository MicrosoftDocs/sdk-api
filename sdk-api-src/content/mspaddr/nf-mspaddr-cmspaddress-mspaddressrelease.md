---
UID: NF:mspaddr.CMSPAddress.MSPAddressRelease
title: CMSPAddress::MSPAddressRelease
author: windows-driver-content
description: The MSPAddressRelease method is the private Release method for the address.
old-location: tapi3\cmspaddress_mspaddressrelease.htm
old-project: Tapi
ms.assetid: 369d6daf-26fb-47f8-b503-6b0e73613bbe
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],MSPAddressRelease method, CMSPAddress.MSPAddressRelease, CMSPAddress::MSPAddressRelease, MSPAddressRelease, MSPAddressRelease method [TAPI 2.2], MSPAddressRelease method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_mspaddressrelease, mspaddr/CMSPAddress::MSPAddressRelease, tapi3.cmspaddress_mspaddressrelease
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSP_EVENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mspaddr.h
api_name:
-	CMSPAddress.MSPAddressRelease
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CMSPAddress::MSPAddressRelease


## -description


The 
<b>MSPAddressRelease</b> method is the private Release method for the address. MSP objects that keep references to the address must call this method instead of the normal COM Release method so that the reference is kept on the MSP address object instead of on the aggregate TAPI address object. This is crucial to ensure correct object lifetimes. A template helper function, <b>MSPReleaseHelper</b>, is provided to help the derived MSP implement this method. All the derived MSP has to do in its implementation of this method is call "MSPReleaseHelper(this)". This is needed simply to provide the type of the derived class to the template helper function.


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

