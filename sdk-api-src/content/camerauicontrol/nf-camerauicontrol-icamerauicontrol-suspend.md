---
UID: NF:camerauicontrol.ICameraUIControl.Suspend
title: ICameraUIControl::Suspend (camerauicontrol.h)
description: Simulates suspend of the user interface control.helpviewer_keywords: ["ICameraUIControl interface [Windows API]","Suspend method","ICameraUIControl.Suspend","ICameraUIControl::Suspend","Suspend","Suspend method [Windows API]","Suspend method [Windows API]","ICameraUIControl interface","camerauicontrol/ICameraUIControl::Suspend","winprog.icamerauicontrol_suspend"]
old-location: winprog\icamerauicontrol_suspend.htm
tech.root: DevNotes
ms.assetid: 864333e6-b17f-4225-9302-4335556d0164
ms.date: 12/05/2018
ms.keywords: ICameraUIControl interface [Windows API],Suspend method, ICameraUIControl.Suspend, ICameraUIControl::Suspend, Suspend, Suspend method [Windows API], Suspend method [Windows API],ICameraUIControl interface, camerauicontrol/ICameraUIControl::Suspend, winprog.icamerauicontrol_suspend
f1_keywords:
- camerauicontrol/ICameraUIControl.Suspend
dev_langs:
- c++
req.header: camerauicontrol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CameraUIControl.idl
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
- camerauicontrol.h
api_name:
- ICameraUIControl.Suspend
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraUIControl::Suspend


## -description


Simulates suspend of the user interface control.


## -parameters




### -param pbDeferralRequired [out]

TRUE if the suspend operation requires deferral; otherwise, FALSE.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nn-camerauicontrol-icamerauicontrol">ICameraUIControl</a>
 

 

