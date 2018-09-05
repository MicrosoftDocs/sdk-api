---
UID: NF:imepad.IImePadApplet.GetAppletConfig
title: GetAppletConfig function
author: windows-sdk-content
description: Called from IImePad to get IImePadApplet's configuration data.
old-location: intl\iimepadapplet_getappletcfg.htm
old-project: Intl
ms.assetid: D24EF900-01D4-4E6E-B752-B11B2F4A6A6C
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: GetAppletCfg method [Internationalization for Windows Applications], GetAppletCfg method [Internationalization for Windows Applications],IImePadApplet interface, GetAppletConfig, IImePadApplet interface [Internationalization for Windows Applications],GetAppletCfg method, IImePadApplet::GetAppletCfg, imepad/IImePadApplet::GetAppletCfg, intl.iimepadapplet_getappletcfg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imepad.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMESTRUCT, *PIMESTRUCT, *NPIMESTRUCT, *LPIMESTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePadApplet.GetAppletCfg
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# GetAppletConfig function


## -description


Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to get <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a>'s configuration data.


## -parameters




### -param lpAppletCfg

Pointer to <a href="https://msdn.microsoft.com/2680231A-0A9C-4723-8E7D-73184C209050">IMEAPPLETCFG</a> structure.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -remarks



This method is called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to get the applet's specific data. This method can be called before calling <a href="https://msdn.microsoft.com/E76FF3FC-717F-42B8-AC5E-45D5527882A7">Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a>



<a href="https://msdn.microsoft.com/2680231A-0A9C-4723-8E7D-73184C209050">IMEAPPLETCFG</a>
 

 

