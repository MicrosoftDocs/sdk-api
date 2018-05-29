---
UID: NF:gpmgmt.IGPMWMIFilter.GetSecurityInfo
title: IGPMWMIFilter::GetSecurityInfo
author: windows-sdk-content
description: Returns an interface or object that represents the list of permissions for the current WMI filter.
old-location: gpmc\igpmwmifilter_getsecurityinfo.htm
old-project: GPMC
ms.assetid: c576c842-53ce-40af-8dba-4f15e25cf493
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMWMIFilter class [GPMC],GetSecurityInfo method, GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],GPMWMIFilter class, GetSecurityInfo method [GPMC],IGPMWMIFilter interface, IGPMWMIFilter interface [GPMC],GetSecurityInfo method, IGPMWMIFilter.GetSecurityInfo, IGPMWMIFilter::GetSecurityInfo, _win32_igpmwmifilter_getsecurityinfo, gpmc.igpmwmifilter_getsecurityinfo, gpmgmt/IGPMWMIFilter::GetSecurityInfo
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMWMIFilter.GetSecurityInfo
-	GPMWMIFilter.GetSecurityInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMWMIFilter::GetSecurityInfo


## -description


Returns an interface or object that represents the list of permissions for the current WMI filter.


## -parameters




### -param ppSecurityInfo [out]

Address of a pointer to an 
<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">GPMSecurityInfo</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">GPMSecurityInfo</a> object.




## -see-also




<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>



<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">IGPMWMIFilterCollection</a>
 

 

