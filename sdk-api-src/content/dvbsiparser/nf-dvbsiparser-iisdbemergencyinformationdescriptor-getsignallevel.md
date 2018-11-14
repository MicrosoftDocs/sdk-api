---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetSignalLevel
title: IIsdbEmergencyInformationDescriptor::GetSignalLevel
author: windows-sdk-content
description: Gets a flag that indicates the emergency alarm signal type from an emergency information descriptor.
old-location: mstv\iisdbemergencyinformationdescriptor_getsignallevel.htm
tech.root: MSTV
ms.assetid: cf0c8d51-4ec8-4dad-8ef3-f18339ed0c0c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSignalLevel, GetSignalLevel method [Microsoft TV Technologies], GetSignalLevel method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetSignalLevel method, IIsdbEmergencyInformationDescriptor.GetSignalLevel, IIsdbEmergencyInformationDescriptor::GetSignalLevel, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetSignalLevel, mstv.iisdbemergencyinformationdescriptor_getsignallevel
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
 - IIsdbEmergencyInformationDescriptor.GetSignalLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IIsdbEmergencyInformationDescriptor.GetSignalLevel
: 
---

# IIsdbEmergencyInformationDescriptor::GetSignalLevel


## -description


Gets a flag that indicates the emergency alarm signal type from an emergency information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the emergency information descriptor that contains the emergency alarm signal. To get the number of emergency information descriptors, call <a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>.


### -param pbVal [out]

Receives a boolean value that indicates whether the emergency alarm signal is the first (0) or second (1) type of start signal. Annex D of the document titled <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM,
ARIB STANDARD,
ARIB STD-B10, Version 4.4</i> describes the two start signal types. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1d098415-1e64-4b49-aa48-654b0d0da5df">IIsdbEmergencyInformationDescriptor</a>



<a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>
 

 

