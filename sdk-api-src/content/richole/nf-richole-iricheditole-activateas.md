---
UID: NF:richole.IRichEditOle.ActivateAs
title: IRichEditOle::ActivateAs
author: windows-sdk-content
description: Handles Activate As behavior by unloading all objects of the old class, telling OLE to treat those objects as objects of the new class, and reloading the objects. If objects cannot be reloaded, they are deleted.
old-location: controls\IRichEditOle_ActivateAs.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleactivateas.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ActivateAs, ActivateAs method [Windows Controls], ActivateAs method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],ActivateAs method, IRichEditOle.ActivateAs, IRichEditOle::ActivateAs, _win32_IRichEditOle_ActivateAs, _win32_IRichEditOle_ActivateAs_cpp, controls.IRichEditOle_ActivateAs, controls._win32_IRichEditOle_ActivateAs, richole/IRichEditOle::ActivateAs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: TEXTRANGEW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	IRichEditOle.ActivateAs
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRichEditOle::ActivateAs


## -description


Handles <b>Activate As</b> behavior by unloading all objects of the old class, telling OLE to treat those objects as objects of the new class, and reloading the objects. If objects cannot be reloaded, they are deleted.


## -parameters




### -param rclsid

Type: <b>REFCLSID</b>

Class identifier of the old class. 


### -param rclsidAs

Type: <b>REFCLSID</b>

Class identifier of the new class. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>
 

 

