---
UID: NF:uiautomationcore.ISynchronizedInputProvider.Cancel
title: ISynchronizedInputProvider::Cancel
author: windows-driver-content
description: Cancels listening for input.
old-location: winauto\uiauto_ISynchronizedInputProvider_Cancel.htm
old-project: WinAuto
ms.assetid: 388fd113-ec66-4152-a42a-a485edcb9b80
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: Cancel, Cancel method [Windows Accessibility], Cancel method [Windows Accessibility],ISynchronizedInputProvider interface, ISynchronizedInputProvider interface [Windows Accessibility],Cancel method, ISynchronizedInputProvider.Cancel, ISynchronizedInputProvider::Cancel, uiauto.uiauto_ISynchronizedInputProvider_Cancel, uiauto_ISynchronizedInputProvider_Cancel, uiautomationcore/ISynchronizedInputProvider::Cancel, winauto.uiauto_ISynchronizedInputProvider_Cancel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	ISynchronizedInputProvider.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISynchronizedInputProvider::Cancel


## -description


Cancels listening for input.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the provider is currently listening for input, it should revert to normal operation.




## -see-also




<a href="https://msdn.microsoft.com/70495eba-172a-432e-951d-1092fd676d5e">ISynchronizedInputProvider</a>
 

 

