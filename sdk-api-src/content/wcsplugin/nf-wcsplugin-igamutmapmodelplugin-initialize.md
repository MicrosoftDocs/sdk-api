---
UID: NF:wcsplugin.IGamutMapModelPlugIn.Initialize
title: IGamutMapModelPlugIn::Initialize
author: windows-sdk-content
description: Initializes a gamut map model profile (GMMP) by using the specified source and destination gamut boundary descriptions and optional source and destination device model plug-ins.
old-location: wcs\IGamutMapModelPlugIn_Initialize.htm
old-project: WCS
ms.assetid: 86fb0f6b-d293-44de-ad1d-724436403535
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IGamutMapModelPlugIn interface [Windows Color System],Initialize method, IGamutMapModelPlugIn.Initialize, IGamutMapModelPlugIn::Initialize, Initialize, Initialize method [Windows Color System], Initialize method [Windows Color System],IGamutMapModelPlugIn interface, _color_IGamutMapModelPlugIn::Initialize, wcs.IGamutMapModelPlugIn_Initialize, wcsplugin/IGamutMapModelPlugIn::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcsplugin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WcsPlugIn.h
api_name:
-	IGamutMapModelPlugIn.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IGamutMapModelPlugIn::Initialize


## -description


Initializes a gamut map model profile (GMMP) by using the specified source and destination gamut boundary descriptions and optional source and destination device model plug-ins.


## -parameters




### -param bstrXml [in]

A string that contains the BSTR XML GMMP profile. This is little-endian Unicode XML, but without the leading bytes to tag it as such. Also, the encoding keyword in the XML may not reflect this format.


### -param pSrcPlugIn [in]

A pointer to a source <a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>. If <b>NULL</b>, it indicates the source device model profile is not a plug-in profile.


### -param pDestPlugIn [in]

A pointer to a destination <a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>. If <b>NULL</b>, it indicates the destination device model profile is not a plug-in profile.


### -param pSrcGBD [in]

A pointer to a source <a href="https://msdn.microsoft.com/b7551967-ff2f-48ed-9346-a75e19fe2c31">GamutBoundaryDescription</a>.


### -param pDestGBD [in]

A pointer to a destination <a href="https://msdn.microsoft.com/b7551967-ff2f-48ed-9346-a75e19fe2c31">GamutBoundaryDescription</a>.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/794eb94c-fdb3-42b3-8320-b13bf51324d1">IGamutMapModelPlugIn</a>
 

 

