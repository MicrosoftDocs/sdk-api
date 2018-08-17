---
UID: NF:camerauicontrol.ICameraUIControl.Suspend
title: ICameraUIControl::Suspend
author: windows-sdk-content
description: Simulates suspend of the user interface control.
old-location: winprog\icamerauicontrol_suspend.htm
old-project: devnotes
ms.assetid: 864333e6-b17f-4225-9302-4335556d0164
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICameraUIControl interface [Windows API],Suspend method, ICameraUIControl.Suspend, ICameraUIControl::Suspend, Suspend, Suspend method [Windows API], Suspend method [Windows API],ICameraUIControl interface, camerauicontrol/ICameraUIControl::Suspend, winprog.icamerauicontrol_suspend
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: camerauicontrol.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CALLFRAME_MARSHALCONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - camerauicontrol.h
api_name:
 - ICameraUIControl.Suspend
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/en-us/library/Hh802717(v=VS.85).aspx">ICameraUIControl</a>
 

 

