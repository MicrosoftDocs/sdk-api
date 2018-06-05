---
UID: NF:dvbsiparser.IPBDAEntitlementDescriptor.GetTag
title: IPBDAEntitlementDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that uniquely identifies an entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.
old-location: mstv\ipbdaentitlementdescriptor_gettag.htm
old-project: mstv
ms.assetid: 484de26a-24e5-431d-ba4d-f2f3005502a1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IPBDAEntitlementDescriptor interface, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies],GetTag method, IPBDAEntitlementDescriptor.GetTag, IPBDAEntitlementDescriptor::GetTag, dvbsiparser/IPBDAEntitlementDescriptor::GetTag, mstv.ipbdaentitlementdescriptor_gettag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IPBDAEntitlementDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDAEntitlementDescriptor::GetTag


## -description


Gets the tag that uniquely identifies an entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.


## -parameters




### -param pbVal [out]

Receives the tag value. For PBDA entitlement descriptors, this value is 0x80.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2fe666fa-ebc4-4a47-87ce-085f357ce186">IPBDAEntitlementDescriptor</a>
 

 

