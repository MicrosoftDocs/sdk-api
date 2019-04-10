---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetTag
title: IIsdbEmergencyInformationDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies an emergency information descriptor.
old-location: mstv\iisdbemergencyinformationdescriptor_gettag.htm
tech.root: mstv
ms.assetid: d0751a09-0336-48d7-a5f0-1182354774a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbEmergencyInformationDescriptor.GetTag, IIsdbEmergencyInformationDescriptor::GetTag, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetTag, mstv.iisdbemergencyinformationdescriptor_gettag
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
 - IIsdbEmergencyInformationDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbEmergencyInformationDescriptor::GetTag


## -description


Gets the tag that identifies an emergency information descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For emergency information descriptors, this value is 0xFC.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1d098415-1e64-4b49-aa48-654b0d0da5df">IIsdbEmergencyInformationDescriptor</a>
 

 

