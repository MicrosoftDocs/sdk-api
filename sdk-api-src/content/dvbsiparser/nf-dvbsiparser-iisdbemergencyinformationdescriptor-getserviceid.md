---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetServiceId
title: IIsdbEmergencyInformationDescriptor::GetServiceId
author: windows-sdk-content
description: Gets the identifier for a broadcasting event from an emergency information descriptor.
old-location: mstv\iisdbemergencyinformationdescriptor_getserviceid.htm
tech.root: MSTV
ms.assetid: 298f0637-eea1-4247-a9ff-cbe1a82fb8f6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetServiceId, GetServiceId method [Microsoft TV Technologies], GetServiceId method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetServiceId method, IIsdbEmergencyInformationDescriptor.GetServiceId, IIsdbEmergencyInformationDescriptor::GetServiceId, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetServiceId, mstv.iisdbemergencyinformationdescriptor_getserviceid
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
 - IIsdbEmergencyInformationDescriptor.GetServiceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbEmergencyInformationDescriptor::GetServiceId


## -description


Gets the identifier for a broadcasting event from an  emergency information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the emergency information descriptor that contains the event identifiers. To get the number of emergency information descriptors, call <a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>



### -param pwVal [out]

Receives the broadcasting event identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1d098415-1e64-4b49-aa48-654b0d0da5df">IIsdbEmergencyInformationDescriptor</a>



<a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>
 

 

