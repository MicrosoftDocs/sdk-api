---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetDataComponentId
title: IIsdbDataContentDescriptor::GetDataComponentId method
author: windows-driver-content
description: Gets a data component identifier from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This identifier identifies a component in the descriptor and appears in the data component descriptor for the component.
old-location: mstv\iisdbdatacontentdescriptor_getdatacomponentid.htm
old-project: mstv
ms.assetid: d8a3e399-5004-41ee-a7eb-4c583a1fdd45
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDataComponentId method [Microsoft TV Technologies], GetDataComponentId method [Microsoft TV Technologies], IIsdbDataContentDescriptor interface, GetDataComponentId,IIsdbDataContentDescriptor.GetDataComponentId, IIsdbDataContentDescriptor, IIsdbDataContentDescriptor interface [Microsoft TV Technologies], GetDataComponentId method, IIsdbDataContentDescriptor::GetDataComponentId, dvbsiparser/IIsdbDataContentDescriptor::GetDataComponentId, mstv.iisdbdatacontentdescriptor_getdatacomponentid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbDataContentDescriptor.GetDataComponentId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDataContentDescriptor::GetDataComponentId method


## -description


Gets a data component identifier from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This identifier identifies a component in the descriptor and appears in the  data component descriptor for the component.


## -parameters




### -param pwVal [out]

Receives the data component identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 

