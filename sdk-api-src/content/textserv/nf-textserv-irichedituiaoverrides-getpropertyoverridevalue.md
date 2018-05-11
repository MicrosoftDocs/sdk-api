---
UID: NF:textserv.IRicheditUiaOverrides.GetPropertyOverrideValue
title: IRicheditUiaOverrides::GetPropertyOverrideValue
author: windows-driver-content
description: Retrieves the host container's override value for the specified Microsoft UI Automation accessibility property of a windowless rich edit control.
old-location: controls\irichedituiaoverrides_getpropertyoverridevalue.htm
old-project: Controls
ms.assetid: C949A3DA-F98E-4035-8986-A76EB8F54558
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetPropertyOverrideValue, GetPropertyOverrideValue method [Windows Controls], GetPropertyOverrideValue method [Windows Controls],IRicheditUiaOverrides interface, IRicheditUiaOverrides interface [Windows Controls],GetPropertyOverrideValue method, IRicheditUiaOverrides.GetPropertyOverrideValue, IRicheditUiaOverrides::GetPropertyOverrideValue, controls.irichedituiaoverrides_getpropertyoverridevalue, textserv/IRicheditUiaOverrides::GetPropertyOverrideValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	IRicheditUiaOverrides.GetPropertyOverrideValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRicheditUiaOverrides::GetPropertyOverrideValue


## -description


Retrieves the host container's override value for the specified Microsoft UI Automation accessibility property of a windowless rich edit control.


## -parameters




### -param propertyId

Type: <b>PROPERTYID </b>

The identifier of the property to retrieve.


### -param pRetValue

Type: <b>VARIANT*</b>

The host container's override value for the <i>propertyId</i> property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2590002F-A6B0-4AA7-A54C-A5AB5304D9FA">IRicheditUiaOverrides</a>
 

 

