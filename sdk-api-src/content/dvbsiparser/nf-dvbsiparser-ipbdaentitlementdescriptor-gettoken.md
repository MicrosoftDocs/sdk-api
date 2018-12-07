---
UID: NF:dvbsiparser.IPBDAEntitlementDescriptor.GetToken
title: IPBDAEntitlementDescriptor::GetToken
author: windows-sdk-content
description: Gets the entitlement token from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.
old-location: mstv\ipbdaentitlementdescriptor_gettoken.htm
tech.root: mstv
ms.assetid: 3fc73b0c-cacb-491b-b25b-49eb57154a37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetToken, GetToken method [Microsoft TV Technologies], GetToken method [Microsoft TV Technologies],IPBDAEntitlementDescriptor interface, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies],GetToken method, IPBDAEntitlementDescriptor.GetToken, IPBDAEntitlementDescriptor::GetToken, dvbsiparser/IPBDAEntitlementDescriptor::GetToken, mstv.ipbdaentitlementdescriptor_gettoken
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDAEntitlementDescriptor.GetToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPBDAEntitlementDescriptor::GetToken


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
 

 

