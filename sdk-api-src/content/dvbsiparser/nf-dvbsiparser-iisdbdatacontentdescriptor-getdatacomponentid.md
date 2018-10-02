---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetDataComponentId
title: IIsdbDataContentDescriptor::GetDataComponentId
author: windows-sdk-content
description: Gets a data component identifier from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This identifier identifies a component in the descriptor and appears in the data component descriptor for the component.
old-location: mstv\iisdbdatacontentdescriptor_getdatacomponentid.htm
tech.root: MSTV
ms.assetid: d8a3e399-5004-41ee-a7eb-4c583a1fdd45
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetDataComponentId, GetDataComponentId method [Microsoft TV Technologies], GetDataComponentId method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetDataComponentId method, IIsdbDataContentDescriptor.GetDataComponentId, IIsdbDataContentDescriptor::GetDataComponentId, dvbsiparser/IIsdbDataContentDescriptor::GetDataComponentId, mstv.iisdbdatacontentdescriptor_getdatacomponentid
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
 - IIsdbDataContentDescriptor.GetDataComponentId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDataContentDescriptor::GetDataComponentId


## -description


Gets a data component identifier from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This identifier identifies a component in the descriptor and appears in the  data component descriptor for the component.


## -parameters




### -param pwVal [out]

Receives the data component identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 

