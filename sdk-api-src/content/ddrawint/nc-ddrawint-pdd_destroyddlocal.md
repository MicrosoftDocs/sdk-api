---
UID: NC:ddrawint.PDD_DESTROYDDLOCAL
title: PDD_DESTROYDDLOCAL (ddrawint.h)
description: The D3dDestroyDDLocal function destroys all the Microsoft Direct3D surfaces previously created by the D3dCreateSurfaceEx function that belong to the same given local Microsoft DirectDraw object.
helpviewer_keywords: ["D3dDestroyDDLocal","D3dDestroyDDLocal callback function [Display Devices]","PDD_DESTROYDDLOCAL","PDD_DESTROYDDLOCAL callback","d3dfncs_3480b8ff-c19d-4495-ab5e-d5ef4e326967.xml","ddrawint/D3dDestroyDDLocal","display.d3ddestroyddlocal"]
old-location: display\d3ddestroyddlocal.htm
tech.root: display
ms.assetid: c68b924b-422d-4a01-8dac-674835833798
ms.date: 12/05/2018
ms.keywords: D3dDestroyDDLocal, D3dDestroyDDLocal callback function [Display Devices], PDD_DESTROYDDLOCAL, PDD_DESTROYDDLOCAL callback, d3dfncs_3480b8ff-c19d-4495-ab5e-d5ef4e326967.xml, ddrawint/D3dDestroyDDLocal, display.d3ddestroyddlocal
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_DESTROYDDLOCAL
 - ddrawint/PDD_DESTROYDDLOCAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - D3dDestroyDDLocal
---

## -description

The <b>D3dDestroyDDLocal</b> function destroys all the Microsoft Direct3D surfaces previously created by the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a> function that belong to the same given local Microsoft DirectDraw object.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddhal_destroyddlocaldata">DDHAL_DESTROYDDLOCALDATA</a> structure that contains the information required for the driver to destroy the surfaces.

## -returns

<b>D3dDestroyDDLocal</b> returns one of the following callback codes:

## -remarks

All Direct3D drivers must support <b>D3dDestroyDDLocal</b>.

Direct3D calls <b>D3dDestroyDDLocal</b> when the application indicates that the Direct3D context is no longer required and it will be destroyed along with all surfaces associated to it. The association comes through the pointer to the local DirectDraw object. The driver must free any memory that the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a> callback allocated for each surface, if necessary. 

The driver should not destroy the DirectDraw surfaces associated with these Direct3D surfaces. This is the application's responsibility.

The pointer to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that was passed in as the <b>lpDDLcl</b> member of the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_contextcreatedata">D3DHAL_CONTEXTCREATEDATA</a> structure when <a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_contextcreatecb">D3dContextCreate</a> was called is released by the operating system after <b>D3dDestroyDDLocal</b> returns. 

<b>D3dDestroyDDLocal</b> can be called with a disabled <a href="/windows-hardware/drivers/">PDEV</a>. A PDEV is disabled or enabled by calling the display driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a> function. See <a href="/windows-hardware/drivers/display/managing-pdevs">Managing PDEVs</a> for more information.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_contextcreatedata">D3DHAL_CONTEXTCREATEDATA</a>



<a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_contextcreatecb">D3dContextCreate</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a>



<a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddhal_destroyddlocaldata">DDHAL_DESTROYDDLOCALDATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a>