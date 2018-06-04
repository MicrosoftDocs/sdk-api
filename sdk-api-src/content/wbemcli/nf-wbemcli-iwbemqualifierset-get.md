---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWbemQualifierSet::Get


## -description


The <b>IWbemQualifierSet::Get</b> method gets the specified named qualifier, if found.


## -parameters




### -param wszName [in]

Name of the qualifier for which the value is being requested. The pointer is treated as read-only.


### -param lFlags [in]

Reserved. This parameter must be 0.


### -param pVal [out]

When successful, <b>VARIANT</b> is assigned to the correct type and value for the qualifier. <b>VariantInit</b> is called on this <b>VARIANT</b>.

It is the responsibility of the caller to call <b>VariantClear</b> on the pointer when the value is no longer required. If there is an error code, the <b>VARIANT</b> pointed to by <i>pVal</i> is not modified.

If this parameter is <b>NULL</b>, the parameter is ignored.


### -param plFlavor [out]

Can be <b>NULL</b>. If not <b>NULL</b>, this must point to a <b>LONG</b> that receives the qualifier flavor bits for the requested qualifier. For more information, see 
<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a> and <a href="https://msdn.microsoft.com/A21ED0FD-1207-42B6-92AE-6080D0E98771">WBEM_FLAVOR_TYPE</a>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>
 

 

