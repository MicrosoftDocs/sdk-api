---
UID: NC:ddrawint.PDD_DESTROYDDLOCAL
title: PDD_DESTROYDDLOCAL
author: windows-driver-content
description: The D3dDestroyDDLocal function destroys all the Microsoft Direct3D surfaces previously created by the D3dCreateSurfaceEx function that belong to the same given local Microsoft DirectDraw object.
old-location: display\d3ddestroyddlocal.htm
old-project: display
ms.assetid: c68b924b-422d-4a01-8dac-674835833798
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: D3dDestroyDDLocal, D3dDestroyDDLocal callback function [Display Devices], PDD_DESTROYDDLOCAL, PDD_DESTROYDDLOCAL callback, d3dfncs_3480b8ff-c19d-4495-ab5e-d5ef4e326967.xml, ddrawint/D3dDestroyDDLocal, display.d3ddestroyddlocal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddrawint.h
api_name:
-	D3dDestroyDDLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_DESTROYDDLOCAL callback function


## -description


The <b>D3dDestroyDDLocal</b> function destroys all the Microsoft Direct3D surfaces previously created by the <a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a> function that belong to the same given local Microsoft DirectDraw object.


## -parameters




### -param Arg1








#### - pcdddd

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549532">DDHAL_DESTROYDDLOCALDATA</a> structure that contains the information required for the driver to destroy the surfaces. 


## -returns



<b>D3dDestroyDDLocal</b> returns one of the following callback codes: 




## -remarks



All Direct3D drivers must support <b>D3dDestroyDDLocal</b>.

Direct3D calls <b>D3dDestroyDDLocal</b> when the application indicates that the Direct3D context is no longer required and it will be destroyed along with all surfaces associated to it. The association comes through the pointer to the local DirectDraw object. The driver must free any memory that the driver's <a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a> callback allocated for each surface, if necessary. 

The driver should not destroy the DirectDraw surfaces associated with these Direct3D surfaces. This is the application's responsibility.

The pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that was passed in as the <b>lpDDLcl</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544739">D3DHAL_CONTEXTCREATEDATA</a> structure when <a href="https://msdn.microsoft.com/c960c3f4-7565-4163-b8c2-a13643110c8c">D3dContextCreate</a> was called is released by the operating system after <b>D3dDestroyDDLocal</b> returns. 

<b>D3dDestroyDDLocal</b> can be called with a disabled <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. A PDEV is disabled or enabled by calling the display driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a> function. See <a href="https://msdn.microsoft.com/f7badbe8-b24f-438a-8937-95bb98de6310">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544739">D3DHAL_CONTEXTCREATEDATA</a>



<a href="https://msdn.microsoft.com/c960c3f4-7565-4163-b8c2-a13643110c8c">D3dContextCreate</a>



<a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549532">DDHAL_DESTROYDDLOCALDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a>
 

 

