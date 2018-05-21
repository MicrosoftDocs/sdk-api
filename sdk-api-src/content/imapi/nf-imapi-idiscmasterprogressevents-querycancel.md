---
UID: NF:imapi.IDiscMasterProgressEvents.QueryCancel
title: IDiscMasterProgressEvents::QueryCancel
author: windows-driver-content
description: Checks whether an AddData, AddAudioTrackBlocks, or RecordDisc operation should be canceled.
old-location: imapi\idiscmasterprogressevents_querycancel.htm
old-project: imapi
ms.assetid: ca7ad8cb-0792-41ec-be5b-147be6750442
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],QueryCancel method, IDiscMasterProgressEvents.QueryCancel, IDiscMasterProgressEvents::QueryCancel, QueryCancel, QueryCancel method [IMAPI], QueryCancel method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_querycancel, base.idiscmasterprogressevents_querycancel, imapi.idiscmasterprogressevents_querycancel, imapi/IDiscMasterProgressEvents::QueryCancel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IDiscMasterProgressEvents.QueryCancel
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMasterProgressEvents::QueryCancel


## -description


Checks whether an 
<a href="https://msdn.microsoft.com/91517103-71c5-450c-9d93-584f94cd2c45">AddData</a>, 
<a href="https://msdn.microsoft.com/d9bd4f3c-4ff5-4f6e-9520-27fef3736636">AddAudioTrackBlocks</a>, or 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a> operation should be canceled.


## -parameters




### -param pbCancel [out]

If this parameter is <b>TRUE</b>, cancel the burn. If this parameter is <b>FALSE</b>, continue the burn.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 

