---
UID: NF:dvbsiparser.IPBDAEntitlementDescriptor.GetToken
title: IPBDAEntitlementDescriptor::GetToken method
author: windows-driver-content
description: Gets the entitlement token from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.
old-location: mstv\ipbdaentitlementdescriptor_gettoken.htm
old-project: mstv
ms.assetid: 3fc73b0c-cacb-491b-b25b-49eb57154a37
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetToken method [Microsoft TV Technologies], GetToken method [Microsoft TV Technologies], IPBDAEntitlementDescriptor interface, GetToken,IPBDAEntitlementDescriptor.GetToken, IPBDAEntitlementDescriptor, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies], GetToken method, IPBDAEntitlementDescriptor::GetToken, dvbsiparser/IPBDAEntitlementDescriptor::GetToken, mstv.ipbdaentitlementdescriptor_gettoken
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IPBDAEntitlementDescriptor.GetToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDAEntitlementDescriptor::GetToken method


## -description


Gets the entitlement token from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.


## -parameters




### -param ppbTokenBuffer [out]

Pointer to a buffer that receives the entitlement token. The caller must free this memory after use.


### -param pdwTokenLength [out]

Receives the entitlement token length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2fe666fa-ebc4-4a47-87ce-085f357ce186">IPBDAEntitlementDescriptor</a>
 

 

