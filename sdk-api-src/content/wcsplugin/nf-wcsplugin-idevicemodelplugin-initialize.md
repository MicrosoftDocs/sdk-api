---
UID: NF:wcsplugin.IDeviceModelPlugIn.Initialize
title: IDeviceModelPlugIn::Initialize
author: windows-sdk-content
description: Takes a pointer to a Stream that contains the whole device model plug-in as input, and initializes any internal parameters required by the plug-in.
old-location: wcs\IDeviceModelPlugIn_Initialize.htm
tech.root: WCS
ms.assetid: ae47dcc5-f771-4586-9086-b4ab1600c1bc
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDeviceModelPlugIn interface [Windows Color System],Initialize method, IDeviceModelPlugIn.Initialize, IDeviceModelPlugIn::Initialize, Initialize, Initialize method [Windows Color System], Initialize method [Windows Color System],IDeviceModelPlugIn interface, _color_IDeviceModelPlugIn::Initialize, wcs.IDeviceModelPlugIn_Initialize, wcsplugin/IDeviceModelPlugIn::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IDeviceModelPlugIn.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceModelPlugIn::Initialize


## -description


Takes a pointer to a Stream that contains the whole device model plug-in as input, and initializes any internal parameters required by the plug-in.


## -parameters




### -param bstrXml [in]

A string that contains the BSTR XML device model plug-in profile. This parameter stores data as little-endian Unicode XML; however, it may have no leading bytes to tag it as such. Also, the encoding keyword in the XML may not reflect that this is formatted as little-endian Unicode. Furthermore, due to the action of the MSXML engine, the BSTR XML file is processed and might not have exactly the same contents as the original XML file.


### -param cNumModels [in]

The number of total models in the transform sequence.


### -param iModelPosition

TBD




#### - uiModelPosition [in]

The one-based model position of the other device model in the workflow of <i>uiNumModels</i> as provided in the <b>Initialize</b> function.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -remarks



If this function is called more than once, subsequent calls release any allocated memory and reinitialize according to the new <i>bstrXml</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

