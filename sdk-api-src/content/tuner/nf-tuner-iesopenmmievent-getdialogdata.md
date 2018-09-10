---
UID: NF:tuner.IESOpenMmiEvent.GetDialogData
title: IESOpenMmiEvent::GetDialogData
author: windows-sdk-content
description: Gets the data associated with an OpenMMI event, in byte stream format. This data can be the contents of the dialog that is opened or the Uniform Resource Locator (URL) that contains the dialog.
old-location: mstv\iesopenmmievent_getdialogdata.htm
tech.root: mstv
ms.assetid: c5deaffb-ceac-4609-a862-b050a1afa1f9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetDialogData, GetDialogData method [Microsoft TV Technologies], GetDialogData method [Microsoft TV Technologies],IESOpenMmiEvent interface, IESOpenMmiEvent interface [Microsoft TV Technologies],GetDialogData method, IESOpenMmiEvent.GetDialogData, IESOpenMmiEvent::GetDialogData, mstv.iesopenmmievent_getdialogdata, tuner/IESOpenMmiEvent::GetDialogData
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESOpenMmiEvent.GetDialogData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESOpenMmiEvent::GetDialogData


## -description


Gets the data associated with an <b>OpenMMI</b> event, in byte stream format. This data can be the contents of the dialog that is opened or the Uniform Resource Locator (URL) that contains the dialog.


## -parameters




### -param pbData [out, retval]

Pointer to a SAFEARRAY object containing the event data. 
          
          The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f54532e2-d1d1-4c6b-ae3d-9f50e0e61366">IESOpenMmiEvent</a>
 

 

