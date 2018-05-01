---
UID: NF:mileffects.IMILBitmapEffectGroupImpl.GetNumberChildren
title: IMILBitmapEffectGroupImpl::GetNumberChildren method
author: windows-driver-content
description: Retrieves the number of children in an effect group.
old-location: wibe\_wibe_imilbitmapeffectgroupimpl_getnumberchildren.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroupimpl\getnumberchildren.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetNumberChildren method [WPF Bitmap Effects], GetNumberChildren method [WPF Bitmap Effects], IMILBitmapEffectGroupImpl interface, GetNumberChildren,IMILBitmapEffectGroupImpl.GetNumberChildren, IMILBitmapEffectGroupImpl, IMILBitmapEffectGroupImpl interface [WPF Bitmap Effects], GetNumberChildren method, IMILBitmapEffectGroupImpl::GetNumberChildren, _wibe_imilbitmapeffectgroupimpl_getnumberchildren, mileffects/IMILBitmapEffectGroupImpl::GetNumberChildren, wibe._wibe_imilbitmapeffectgroupimpl_getnumberchildren
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectGroupImpl.GetNumberChildren
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectGroupImpl::GetNumberChildren method


## -description


Retrieves the number of children in an effect group.


## -parameters




### -param puiNumberChildren [out, retval]

Type: <b>ULONG*</b>

A pointer that receives the number of effects in the group.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



