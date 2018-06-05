---
UID: NF:gpmgmt.IGPMWMIFilter.SetSecurityInfo
title: IGPMWMIFilter::SetSecurityInfo
author: windows-sdk-content
description: Sets the list of permissions for the current WMI filter to that specified by the object.
old-location: gpmc\igpmwmifilter_setsecurityinfo.htm
old-project: GPMC
ms.assetid: e03af7ce-dec8-4390-9880-6f5ff050ca0c
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMWMIFilter object [GPMC],SetSecurityInfo method, IGPMWMIFilter interface [GPMC],SetSecurityInfo method, IGPMWMIFilter.SetSecurityInfo, IGPMWMIFilter::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],GPMWMIFilter object, SetSecurityInfo method [GPMC],IGPMWMIFilter interface, _win32_igpmwmifilter_setsecurityinfo, gpmc.igpmwmifilter_setsecurityinfo, gpmgmt/IGPMWMIFilter::SetSecurityInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMWMIFilter.SetSecurityInfo
-	GPMWMIFilter.SetSecurityInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMWMIFilter::SetSecurityInfo


## -description


Sets the list of permissions for the current WMI filter to that specified by the object.


## -parameters




### -param pSecurityInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a> interface.  This parameter is required.


#### - objGPMSecurityInfo [in]


<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">GPMSecurityInfo</a> object to set. This parameter is required.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



You should understand these considerations before changing permissions on WMI filters.

<ul>
<li>Read permission is required for all users to whom a WMI filter applies. Authenticated users always have read access to all WMI filters. Typically, all users to whom the GPO with the WMI filter link applies also have read access.</li>
<li>Users with permission to edit WMI filters can affect policy processing for all users to whom the WMI filter applies.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>



<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">IGPMWMIFilterCollection</a>
 

 

