---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetAreaCode
title: IIsdbEmergencyInformationDescriptor::GetAreaCode
author: windows-sdk-content
description: Gets the area codes from an emergency information descriptor.
old-location: mstv\iisdbemergencyinformationdescriptor_getareacode.htm
tech.root: mstv
ms.assetid: 7bf09adf-6a04-4c3a-8c66-aea4e96c6936
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetAreaCode, GetAreaCode method [Microsoft TV Technologies], GetAreaCode method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetAreaCode method, IIsdbEmergencyInformationDescriptor.GetAreaCode, IIsdbEmergencyInformationDescriptor::GetAreaCode, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetAreaCode, mstv.iisdbemergencyinformationdescriptor_getareacode
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
 - IIsdbEmergencyInformationDescriptor.GetAreaCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbEmergencyInformationDescriptor::GetAreaCode


## -description


Gets the area codes from an emergency information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the emergency information descriptor that contains the area code records. To get the number of area code records, call <a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>.


### -param ppwVal [out]

Pointer to a buffer allocated to hold the area codes. The caller is responsible for freeing this memory.


### -param pbNumAreaCodes [out]

Receives the number of area codes in the descriptor.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For more information about area codes and their use with emergency broadcast signals, refer to Annex D of the document titled <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM,
ARIB STANDARD,
ARIB STD-B10, Version 4.4</i>.




## -see-also




<a href="https://msdn.microsoft.com/1d098415-1e64-4b49-aa48-654b0d0da5df">IIsdbEmergencyInformationDescriptor</a>



<a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>
 

 

