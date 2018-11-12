---
UID: NF:mfapi.MFGetPluginControl
title: MFGetPluginControl function
author: windows-sdk-content
description: Gets a pointer to the Microsoft Media Foundation plug-in manager.
old-location: mf\mfgetplugincontrol.htm
tech.root: medfound
ms.assetid: 68b25c68-806d-46c3-98f8-8f29d7c21471
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFGetPluginControl, MFGetPluginControl function [Media Foundation], mf.mfgetplugincontrol, mfapi/MFGetPluginControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetPluginControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetPluginControl function


## -description


Gets a pointer to the Microsoft Media Foundation plug-in manager.


## -parameters




### -param ppPluginControl [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

