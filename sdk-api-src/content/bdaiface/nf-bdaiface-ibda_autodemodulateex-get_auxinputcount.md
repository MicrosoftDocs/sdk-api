---
UID: NF:bdaiface.IBDA_AutoDemodulateEx.get_AuxInputCount
title: IBDA_AutoDemodulateEx::get_AuxInputCount
author: windows-sdk-content
description: The get_AuxInputCount method retrieves a count of the number of auxiliary inputs on the demodulator.
old-location: mstv\ibda_autodemodulateex_get_auxinputcount.htm
old-project: mstv
ms.assetid: a23a1d54-377e-48cb-a4ff-dfd5a6972677
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IBDA_AutoDemodulateEx interface [Microsoft TV Technologies],get_AuxInputCount method, IBDA_AutoDemodulateEx.get_AuxInputCount, IBDA_AutoDemodulateEx::get_AuxInputCount, IBDA_AutoDemodulateExget_AuxInputCount, bdaiface/IBDA_AutoDemodulateEx::get_AuxInputCount, get_AuxInputCount, get_AuxInputCount method [Microsoft TV Technologies], get_AuxInputCount method [Microsoft TV Technologies],IBDA_AutoDemodulateEx interface, mstv.ibda_autodemodulateex_get_auxinputcount
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
 - IBDA_AutoDemodulateEx.get_AuxInputCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_AutoDemodulateEx::get_AuxInputCount


## -description


The <b>get_AuxInputCount</b> method retrieves a count of the number of auxiliary inputs on the demodulator.


## -parameters




### -param pulCompositeCount [in, out]

Pointer to a variable that receives a count of the number of composite-video input connectors on the device.


### -param pulSvideoCount [in, out]

Pointer to a variable that receives a count of the number of S-Video input connectors on the device.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



<div class="alert"><b>Note</b>  The <i>pulCompositeCount</i> and <i>pulSvideoCount</i> parameters are marked in the IDL file as [in, out] but are used as [out] parameters. To preserve binary compatibility with previous versions, they have not been changed.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ecc642e4-7c36-400c-8a63-639f75b2bbc2">IBDA_AutoDemodulateEx Interface</a>
 

 

