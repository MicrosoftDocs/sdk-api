---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetServiceIds
title: IIsdbCAServiceDescriptor::GetServiceIds
author: windows-driver-content
description: Gets the service identifier (ID) records from a conditional access (CA) service descriptor.
old-location: mstv\iisdbcaservicedescriptor_getserviceids.htm
old-project: mstv
ms.assetid: f2a6d1f2-2cd5-4f8c-97e1-33880ffb0449
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetServiceIds, GetServiceIds method [Microsoft TV Technologies], GetServiceIds method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetServiceIds method, IIsdbCAServiceDescriptor.GetServiceIds, IIsdbCAServiceDescriptor::GetServiceIds, dvbsiparser/IIsdbCAServiceDescriptor::GetServiceIds, mstv.iisdbcaservicedescriptor_getserviceids
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
-	IIsdbCAServiceDescriptor.GetServiceIds
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbCAServiceDescriptor::GetServiceIds


## -description


Gets the service identifier (ID) records from a conditional access (CA) service descriptor.


## -parameters




### -param pbNumServiceIds [in, out]

On input specifies the expected number of service ID records. On output returns the actual number of records.


### -param pwServiceIds [out]

Receives the service ID records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6d56e39d-3c7a-4c55-8d07-00e25eba18bd">IIsdbCAServiceDescriptor</a>
 

 

