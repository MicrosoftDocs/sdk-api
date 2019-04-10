---
UID: NF:gpmgmt.IGPMDomain.GetWMIFilter
title: IGPMDomain::GetWMIFilter (gpmgmt.h)
author: windows-sdk-content
description: Retrieves a GPMWMIFilter object for the specified path.
old-location: gpmc\igpmdomain_getwmifilter.htm
tech.root: gpmc
ms.assetid: 093fba1a-69b3-4045-891a-de9c6a78e166
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],GetWMIFilter method, GetWMIFilter, GetWMIFilter method [GPMC], GetWMIFilter method [GPMC],GPMDomain object, GetWMIFilter method [GPMC],IGPMDomain interface, IGPMDomain interface [GPMC],GetWMIFilter method, IGPMDomain.GetWMIFilter, IGPMDomain::GetWMIFilter, _win32_igpmdomain_getwmifilter, gpmc.igpmdomain_getwmifilter, gpmgmt/IGPMDomain::GetWMIFilter
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMDomain.GetWMIFilter
 - GPMDomain.GetWMIFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain::GetWMIFilter


## -description


Retrieves a 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object for the specified path.


## -parameters




### -param bstrPath [in]

Path of the <a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object to retrieve, in the following format: MSFT_SomFilter.Domain="<i>&lt;domain of the WMI filter&gt;</i>", ID="<i>&lt;GUID that represents the WMI filter&gt;</i>". Consider this example: MSFT_SomFilter.Domain="example.microsoft.com", ID="{7ab06d20-5e0a-4de9-8170-13dea779a528}".


### -param ppWMIFilter [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>
 

 

