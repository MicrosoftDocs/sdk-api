---
UID: NE:shcore.BSOS_OPTIONS
title: BSOS_OPTIONS
author: windows-sdk-content
description: Specifies the behavior of a RandomAccessStream that encapsulates a Component Object Model (COM) IStream.
old-location: winrt\bsos_options.htm
old-project: WinRT
ms.assetid: C51D945B-37C6-44CB-BF80-5FA62EE1F477
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: BSOS_DEFAULT, BSOS_OPTIONS, BSOS_OPTIONS enumeration [Windows Runtime], BSOS_PREFERDESTINATIONSTREAM, shcore/BSOS_DEFAULT, shcore/BSOS_OPTIONS, shcore/BSOS_PREFERDESTINATIONSTREAM, winrt.bsos_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shcore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BSOS_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shcore.h
api_name:
-	BSOS_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# BSOS_OPTIONS enumeration


## -description


Specifies the behavior of a <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> that encapsulates a Component Object Model (COM) <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


## -enum-fields




### -field BSOS_DEFAULT

When creating a <a href="https://msdn.microsoft.com/dec8e90e-2cbb-497c-ad7f-c77c713af83c">RandomAccessStream</a> over a stream, use the base <a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a> behavior on the <a href="https://msdn.microsoft.com/f55c376b-f150-406a-b960-f096c2deeff1">STGM</a> mode from the <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a> method.


### -field BSOS_PREFERDESTINATIONSTREAM

Use the <a href="https://msdn.microsoft.com/4903a3a1-12b7-4094-aac8-6e8525998c3c">GetDestinationStream</a> method.


## -see-also




<a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

