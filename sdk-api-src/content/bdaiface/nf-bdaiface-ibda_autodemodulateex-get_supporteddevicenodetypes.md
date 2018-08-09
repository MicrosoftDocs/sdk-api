---
UID: NF:bdaiface.IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes
title: IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes
author: windows-sdk-content
description: The get_SupportedDeviceNodeTypes method retrieves a list of the device node types that the demodulator supports.
old-location: mstv\ibda_autodemodulateex_get_supporteddevicenodetypes.htm
old-project: mstv
ms.assetid: 94d105f5-a609-4c10-b63e-61e39ee66fd3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_AutoDemodulateEx interface [Microsoft TV Technologies],get_SupportedDeviceNodeTypes method, IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes, IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes, IBDA_AutoDemodulateExget_SupportedDeviceNodeTypes, bdaiface/IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes, get_SupportedDeviceNodeTypes, get_SupportedDeviceNodeTypes method [Microsoft TV Technologies], get_SupportedDeviceNodeTypes method [Microsoft TV Technologies],IBDA_AutoDemodulateEx interface, mstv.ibda_autodemodulateex_get_supporteddevicenodetypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_AutoDemodulateEx.get_SupportedDeviceNodeTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes


## -description


The <b>get_SupportedDeviceNodeTypes</b> method retrieves a list of the device node types that the demodulator supports.


## -parameters




### -param ulcDeviceNodeTypesMax [in]

Specifies the size of the <i>pguidDeviceNodeTypes</i> array.


### -param pulcDeviceNodeTypes [out]

If <i>pguidDeviceNodeTypes</i> is <b>NULL</b>, receives the number of device node types that the demodulator supports. If <i>pguidDeviceNodeTypes</i> is not <b>NULL</b>, receives the number of node types that were copied into the <i>pguidDeviceNodeTypes</i> array.


### -param pguidDeviceNodeTypes [in, out]

Pointer to an array of GUIDs, or <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If <i>pguidDeviceNodeTypes</i> is <b>NULL</b>, the method returns the number of supported node types in the <i>pulcDeviceNodeTypes</i> parameter. Otherwise, the method copies the node types into the <i>pguidDeviceNodeTypes</i> array, up to a maximum of <i>ulcDeviceNodeTypesMax</i>.




## -see-also




<a href="https://msdn.microsoft.com/ecc642e4-7c36-400c-8a63-639f75b2bbc2">IBDA_AutoDemodulateEx Interface</a>
 

 

