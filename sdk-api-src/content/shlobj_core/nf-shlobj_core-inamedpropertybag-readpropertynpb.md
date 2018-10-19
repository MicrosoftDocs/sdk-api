---
UID: NF:shlobj_core.INamedPropertyBag.ReadPropertyNPB
title: INamedPropertyBag::ReadPropertyNPB
author: windows-sdk-content
description: Causes a property to be read from the named property bag.
old-location: shell\INamedPropertyBag_ReadPropertyNPB.htm
tech.root: shell
ms.assetid: 7080edeb-4908-4b0a-9416-9b301c54bb4c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: INamedPropertyBag interface [Windows Shell],ReadPropertyNPB method, INamedPropertyBag.ReadPropertyNPB, INamedPropertyBag::ReadPropertyNPB, ReadPropertyNPB, ReadPropertyNPB method [Windows Shell], ReadPropertyNPB method [Windows Shell],INamedPropertyBag interface, _shell_INamedPropertyBag_ReadPropertyNPB, shell.INamedPropertyBag_ReadPropertyNPB, shlobj_core/INamedPropertyBag::ReadPropertyNPB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
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
req.lib: 
req.dll: Shdocvw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - INamedPropertyBag.ReadPropertyNPB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamedPropertyBag::ReadPropertyNPB


## -description


Causes a property to be read from the named property bag.


## -parameters




### -param pszBagname

TBD


### -param pszPropName [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property to be read.


### -param pVar [in, out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

The address of a <b>VARIANT</b> that, when this method returns successfully, receives the property value.


#### - pszBagName [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property bag.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



