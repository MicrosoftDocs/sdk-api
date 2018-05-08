---
UID: NF:tuner.IESOpenMmiEvent.GetDialogType
title: IESOpenMmiEvent::GetDialogType
author: windows-driver-content
description: The GetDialogType method gets the GUID representing the experience type of the dialog that is being opened.
old-location: mstv\iesopenmmievent_getdialogtype.htm
old-project: mstv
ms.assetid: 93f3cd5e-7d8e-42b9-a688-3df22855e7fb
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDialogType, GetDialogType method [Microsoft TV Technologies], GetDialogType method [Microsoft TV Technologies],IESOpenMmiEvent interface, IESOpenMmiEvent interface [Microsoft TV Technologies],GetDialogType method, IESOpenMmiEvent.GetDialogType, IESOpenMmiEvent::GetDialogType, mstv.iesopenmmievent_getdialogtype, tuner/IESOpenMmiEvent::GetDialogType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESOpenMmiEvent.GetDialogType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESOpenMmiEvent::GetDialogType


## -description



      The <b>GetDialogType</b> method gets the GUID representing the experience type of the dialog that is being opened. 


## -parameters




### -param guidDialogType [out, retval]


            Gets the GUID identifying the experience type of the dialog. If the application does not recognize the experience type, it should set the event as complete  by returning an ERROR_ INVALID_TYPE result.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f54532e2-d1d1-4c6b-ae3d-9f50e0e61366">IESOpenMmiEvent</a>
 

 

