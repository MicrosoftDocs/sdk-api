---
UID: NF:wiautil.wiauPropsInPropSpec
title: wiauPropsInPropSpec function
author: windows-driver-content
description: The wiauPropsInPropSpec function determines whether any of a list of property specification IDs is contained within an array of such values.
old-location: image\wiaupropsinpropspec.htm
old-project: image
ms.assetid: c376297a-11a6-4e9f-b551-36a573cdb7e0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaupropsinpropspec, wiauFncs_2490b5b3-8051-4711-b681-1aef18580182.xml, wiauPropsInPropSpec, wiauPropsInPropSpec function [Imaging Devices], wiautil/wiauPropsInPropSpec
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiautil.h
api_name:
-	wiauPropsInPropSpec
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauPropsInPropSpec function


## -description


The <b>wiauPropsInPropSpec</b> function determines whether any of a list of property specification IDs is contained within an array of such values.


## -parameters




### -param NumPropSpecs

Specifies the number of property specification IDs in the array pointed to by the <i>pPropSpecs</i> parameter.


### -param pPropSpecs [in]

Points to the first element of the array of property specification IDs.


### -param NumProps

Specifies the number of property specification IDs to search for.


### -param pProps [in]

Points to the first element of the array containing the property specification IDs to search for.


## -returns



This function returns <b>TRUE</b> as soon as it finds one of the property specification IDs given in the <i>pProps</i> array in the <i>pPropSpecs</i> array. If the function is unable to find any of the listed property specification IDs in that array, it returns <b>FALSE</b>.




## -remarks



The <b>wiauPropsInPropSpec</b> function finds one or more property specification IDs within an array of property specification IDs. A related function, <a href="https://msdn.microsoft.com/library/windows/hardware/ff550171">wiauPropInPropSpec</a>, can be used to find a single property specification ID within such an array.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550171">wiauPropInPropSpec</a>
 

 

