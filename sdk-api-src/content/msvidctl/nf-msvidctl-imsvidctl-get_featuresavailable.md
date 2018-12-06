---
UID: NF:msvidctl.IMSVidCtl.get_FeaturesAvailable
title: IMSVidCtl::get_FeaturesAvailable
author: windows-sdk-content
description: The get_FeaturesAvailable method retrieves the features that are available on the local system.
old-location: mstv\imsvidctl_get_featuresavailable.htm
tech.root: mstv
ms.assetid: 73da686c-0c25-4dfb-8a13-681f1dac6a4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_FeaturesAvailable method, IMSVidCtl.get_FeaturesAvailable, IMSVidCtl::get_FeaturesAvailable, IMSVidCtlget_FeaturesAvailable, get_FeaturesAvailable, get_FeaturesAvailable method [Microsoft TV Technologies], get_FeaturesAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_featuresavailable, msvidctl/IMSVidCtl::get_FeaturesAvailable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - msvidctl.h
api_name:
 - IMSVidCtl.get_FeaturesAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get_FeaturesAvailable


## -description


The <b>get_FeaturesAvailable</b> method retrieves the features that are available on the local system.


## -parameters




### -param pVal [out]

Receives an <a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns a collection of feature objects. Use the returned <a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures</a> pointer to enumerate the collection. To activate a feature, add it to the active features collection. To search for a specific feature, call the <a href="https://msdn.microsoft.com/80890372-2d92-4a3a-963f-2a6ca6632c52">IMSVidDevice::get__ClassID</a> method on each feature and compare the result against the CLSID of the feature you are looking for.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>
 

 

