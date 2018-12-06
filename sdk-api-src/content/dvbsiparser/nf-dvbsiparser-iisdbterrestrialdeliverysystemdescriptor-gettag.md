---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetTag
title: IIsdbTerrestrialDeliverySystemDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies an Integrated Digital Services Broadcasting (ISDB) terrestrial delivery system descriptor.
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 15b70e2e-21e0-406c-9d7a-32031114d50b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbTerrestrialDeliverySystemDescriptor.GetTag, IIsdbTerrestrialDeliverySystemDescriptor::GetTag, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetTag, mstv.iisdbterrestrialdeliverysystemdescriptor_gettag
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
 - IIsdbTerrestrialDeliverySystemDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Digital Services Broadcasting (ISDB) terrestrial delivery system descriptor.


## -parameters




### -param pbVal [out]

Receives the terrestrial delivery system descriptor tag. For terrestrial delivery system descriptors, this value is 0xFA.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32bde3dd-05e0-466b-9f04-4b55b0d7f374">IIsdbTerrestrialDeliverySystemDescriptor</a>
 

 

