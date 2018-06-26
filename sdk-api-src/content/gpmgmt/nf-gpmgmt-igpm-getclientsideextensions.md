---
UID: NF:gpmgmt.IGPM.GetClientSideExtensions
title: IGPM::GetClientSideExtensions
author: windows-sdk-content
description: Creates and returns a GPMCSECollection object that allows you to enumerate Group Policy client-side extensions (CSEs) that are registered on the local computer.
old-location: gpmc\igpm_getclientsideextensions.htm
old-project: GPMC
ms.assetid: 5bcf76f5-f216-4a33-9ac1-4cb98eb26db5
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GPM object [GPMC],GetClientSideExtensions method, GetClientSideExtensions, GetClientSideExtensions method [GPMC], GetClientSideExtensions method [GPMC],GPM object, GetClientSideExtensions method [GPMC],IGPM interface, IGPM interface [GPMC],GetClientSideExtensions method, IGPM.GetClientSideExtensions, IGPM::GetClientSideExtensions, _win32_igpm_getclientsideextensions, gpmc.igpm_getclientsideextensions, gpmgmt/IGPM::GetClientSideExtensions
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM.GetClientSideExtensions
 - GPM.GetClientSideExtensions
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::GetClientSideExtensions


## -description


Creates and returns a 
<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">GPMCSECollection</a> object that allows you to enumerate Group Policy client-side extensions (CSEs) that are registered on the local computer.


## -parameters




### -param ppIGPMCSECollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">IGPMCSECollection</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMCSECollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMCSECollection</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">IGPMCSECollection</a>
 

 

