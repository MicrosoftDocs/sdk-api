---
UID: NF:wia_xp.IEnumWIA_DEV_INFO.Clone
title: IEnumWIA_DEV_INFO::Clone
author: windows-sdk-content
description: The IEnumWIA_DEV_INFO::Clone method creates an additional instance of the IEnumWIA_DEV_INFO interface and sends back a pointer to it.
old-location: wia\_wia_IEnumWIA_DEV_INFO_Clone.htm
old-project: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwia_dev_info\clone.htm
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: Clone, Clone method [WIA], Clone method [WIA],IEnumWIA_DEV_INFO interface, IEnumWIA_DEV_INFO interface [WIA],Clone method, IEnumWIA_DEV_INFO.Clone, IEnumWIA_DEV_INFO::Clone, _wia_IEnumWIA_DEV_INFO_Clone, wia._wia_IEnumWIA_DEV_INFO_Clone, wia_xp/IEnumWIA_DEV_INFO::Clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IEnumWIA_DEV_INFO.Clone
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWIA_DEV_INFO::Clone


## -description


The <b>IEnumWIA_DEV_INFO::Clone</b> method creates an additional instance of the <a href="https://msdn.microsoft.com/2133b9a4-9340-4984-a81e-66587f2e5163">IEnumWIA_DEV_INFO</a> interface and sends back a pointer to it.



## -parameters




### -param ppIEnum [out]

Type: <b><a href="https://msdn.microsoft.com/2133b9a4-9340-4984-a81e-66587f2e5163">IEnumWIA_DEV_INFO</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/2133b9a4-9340-4984-a81e-66587f2e5163">IEnumWIA_DEV_INFO</a> interface. This parameter contains a pointer to the <b>IEnumWIA_DEV_INFO</b> interface instance that <b>IEnumWIA_DEV_INFO::Clone</b> creates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the pointers they receive through the <i>ppIEnum</i> parameter.



