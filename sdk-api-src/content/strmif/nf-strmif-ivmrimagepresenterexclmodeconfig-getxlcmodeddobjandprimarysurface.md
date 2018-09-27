---
UID: NF:strmif.IVMRImagePresenterExclModeConfig.GetXlcModeDDObjAndPrimarySurface
title: IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface
author: windows-sdk-content
description: The GetXlcModeDDObjAndPrimarySurface method retrieves the DirectDraw object and primary surface currently being used by a VMR that has been configured for DirectDraw Exclusive Mode using the SetXlcModeDDObjAndPrimarySurface method.
old-location: dshow\ivmrimagepresenterexclmodeconfig_getxlcmodeddobjandprimarysurface.htm
tech.root: DirectShow
ms.assetid: 09b756de-7fd2-44d8-9ef3-6b5dc56cb8b3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetXlcModeDDObjAndPrimarySurface, GetXlcModeDDObjAndPrimarySurface method [DirectShow], GetXlcModeDDObjAndPrimarySurface method [DirectShow],IVMRImagePresenterExclModeConfig interface, IVMRImagePresenterExclModeConfig interface [DirectShow],GetXlcModeDDObjAndPrimarySurface method, IVMRImagePresenterExclModeConfig.GetXlcModeDDObjAndPrimarySurface, IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface, dshow.ivmrimagepresenterexclmodeconfig_getxlcmodeddobjandprimarysurface, strmif/IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRImagePresenterExclModeConfig.GetXlcModeDDObjAndPrimarySurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface


## -description



The <code>GetXlcModeDDObjAndPrimarySurface</code> method retrieves the DirectDraw object and primary surface currently being used by a VMR that has been configured for DirectDraw Exclusive Mode using the <b>SetXlcModeDDObjAndPrimarySurface</b> method.




## -parameters




### -param lpDDObj [out]

Retrieves the Exclusive Mode DirectDraw object created by the application.


### -param lpPrimarySurf [out]

Retrieves the primary surface associated with the DirectDraw object.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The procedure for configuring and using an application-defined DirectDraw Exclusive Mode object is described in <a href="https://msdn.microsoft.com/3ef4f267-4dc2-421b-ade4-6b1efa364733">DirectDraw Exclusive Mode</a>.




## -see-also




<a href="https://msdn.microsoft.com/67c9675c-c0fd-44f6-bdeb-ac3f73e937cc">IVMRImagePresenterExclModeConfig Interface</a>



<a href="https://msdn.microsoft.com/3af69975-fe3c-45e6-b1f5-ce2dbda9a4dc">IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

