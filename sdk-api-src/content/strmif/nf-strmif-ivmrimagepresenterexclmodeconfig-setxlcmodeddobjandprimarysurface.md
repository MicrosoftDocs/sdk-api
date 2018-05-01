---
UID: NF:strmif.IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface
title: IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface method
author: windows-driver-content
description: The SetXlcModeDDObjAndPrimarySurface method informs the VMR of the DirectDraw object and primary surface that were created by the application.
old-location: dshow\ivmrimagepresenterexclmodeconfig_setxlcmodeddobjandprimarysurface.htm
old-project: DirectShow
ms.assetid: 3af69975-fe3c-45e6-b1f5-ce2dbda9a4dc
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVMRImagePresenterExclModeConfig, IVMRImagePresenterExclModeConfig interface [DirectShow], SetXlcModeDDObjAndPrimarySurface method, IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface, SetXlcModeDDObjAndPrimarySurface, SetXlcModeDDObjAndPrimarySurface method [DirectShow], SetXlcModeDDObjAndPrimarySurface method [DirectShow], IVMRImagePresenterExclModeConfig interface, SetXlcModeDDObjAndPrimarySurface,IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface, dshow.ivmrimagepresenterexclmodeconfig_setxlcmodeddobjandprimarysurface, strmif/IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface method


## -description



The <code>SetXlcModeDDObjAndPrimarySurface</code> method informs the VMR of the DirectDraw object and primary surface that were created by the application.




## -parameters




### -param lpDDObj [in]

Specifies the Exclusive Mode DirectDraw object created by the application.


### -param lpPrimarySurf [in]

Specifies the primary surface associated with the DirectDraw object.


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



<a href="https://msdn.microsoft.com/09b756de-7fd2-44d8-9ef3-6b5dc56cb8b3">IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

