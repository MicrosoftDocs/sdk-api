---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetStartEndFlag
title: IIsdbEmergencyInformationDescriptor::GetStartEndFlag
author: windows-sdk-content
description: Gets the value of the start_end_flag field from an emergency information descriptor. This field indicates whether the emergency alarm signal has started or finished broadcasting.
old-location: mstv\iisdbemergencyinformationdescriptor_getstartendflag.htm
old-project: mstv
ms.assetid: 13593be1-073c-41df-b389-f0920d192c92
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetStartEndFlag, GetStartEndFlag method [Microsoft TV Technologies], GetStartEndFlag method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetStartEndFlag method, IIsdbEmergencyInformationDescriptor.GetStartEndFlag, IIsdbEmergencyInformationDescriptor::GetStartEndFlag, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetStartEndFlag, mstv.iisdbemergencyinformationdescriptor_getstartendflag
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbEmergencyInformationDescriptor.GetStartEndFlag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbEmergencyInformationDescriptor::GetStartEndFlag


## -description


 Gets the value of the start_end_flag field from an emergency information descriptor. This field indicates whether the emergency alarm signal has started or finished broadcasting.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the service information (SI) descriptor containing the table descriptor. To get the number of SI descriptors, call <a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>



### -param pVal [out]

Gets the start/end flag from the descriptor. If this value is 1, the emergency signal has started or is being broadcast. If it is 0, the emergency signal broadcast has ended. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1d098415-1e64-4b49-aa48-654b0d0da5df">IIsdbEmergencyInformationDescriptor</a>



<a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>
 

 

