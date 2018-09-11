---
UID: NF:d2d1_1helper.CreationProperties
title: CreationProperties function
author: windows-sdk-content
description: Returns a D2D1_CREATION_PROPERTIES that describes root-level creation details.
old-location: direct2d\creationproperties.htm
tech.root: direct2d
ms.assetid: 81D88AFE-77B9-4871-9832-7323CAAB39CF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreationProperties, CreationProperties function [Direct2D], d2d1_1helper/CreationProperties, direct2d.creationproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - CreationProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreationProperties function


## -description


Returns a  <a href="https://msdn.microsoft.com/en-us/library/Hh404298(v=VS.85).aspx">D2D1_CREATION_PROPERTIES</a> that describes root-level creation details.


## -parameters




### -param threadingMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh447020(v=VS.85).aspx">D2D1_THREADING_MODE</a></b>

The threading mode with which the corresponding root objects are created.


### -param debugLevel

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368090(v=VS.85).aspx">D2D1_DEBUG_LEVEL</a></b>

The debug level that the root objects should be created with.


### -param options

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh446998(v=VS.85).aspx">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The device context options that the root objects should be created with.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh404298(v=VS.85).aspx">D2D1_CREATION_PROPERTIES</a></b>

The filled creation properties structure.



