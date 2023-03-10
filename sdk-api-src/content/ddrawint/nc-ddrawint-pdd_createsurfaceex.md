---
UID: NC:ddrawint.PDD_CREATESURFACEEX
title: PDD_CREATESURFACEEX (ddrawint.h)
description: The D3dCreateSurfaceEx function notifies about the association of a Microsoft DirectDraw surface and a Microsoft Direct3D handle value to enable setting up the surface for Direct3D rendering.
helpviewer_keywords: ["D3dCreateSurfaceEx","D3dCreateSurfaceEx callback function [Display Devices]","PDD_CREATESURFACEEX","PDD_CREATESURFACEEX callback","d3dfncs_84d5da96-838e-4ba9-84a2-412e58f36bd0.xml","ddrawint/D3dCreateSurfaceEx","display.d3dcreatesurfaceex"]
old-location: display\d3dcreatesurfaceex.htm
tech.root: display
ms.assetid: dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813
ms.date: 12/05/2018
ms.keywords: D3dCreateSurfaceEx, D3dCreateSurfaceEx callback function [Display Devices], PDD_CREATESURFACEEX, PDD_CREATESURFACEEX callback, d3dfncs_84d5da96-838e-4ba9-84a2-412e58f36bd0.xml, ddrawint/D3dCreateSurfaceEx, display.d3dcreatesurfaceex
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
 - PDD_CREATESURFACEEX
 - ddrawint/PDD_CREATESURFACEEX
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
 - D3dCreateSurfaceEx
---

## -description

The <b>D3dCreateSurfaceEx</b> function notifies about the association of a Microsoft DirectDraw surface and a Microsoft Direct3D handle value to enable setting up the surface for Direct3D rendering.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata">DD_CREATESURFACEEXDATA</a> structure that contains the information required for the driver to create the surface.

## -returns

<b>D3dCreateSurfaceEx</b> returns one of the following callback codes:

## -remarks

All Direct3D drivers must support <b>D3dCreateSurfaceEx</b>.

<b>D3dCreateSurfaceEx</b> creates an association between a DirectDraw surface and a small integer surface handle. By creating these associations between a handle and a DirectDraw surface, <b>D3dCreateSurfaceEx</b> allows a surface handle to be embedded in the Direct3D command stream. For example, when the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DDP2OP_TEXBLT</a> command token is sent to the driver's <a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a> function to load a texture map, it uses a source handle and destination handle that were associated with a DirectDraw surface through <b>D3dCreateSurfaceEx</b>. 

For every DirectDraw surface created under the local DirectDraw object, the runtime generates a valid handle that uniquely identifies the surface and places the handle in the <b>dwSurfaceHandle</b> member of a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_more">DD_SURFACE_MORE</a> structure. The <b>lpDDSLcl</b> member of the DD_CREATESURFACEEXDATA structure at <i>pcsxd</i> points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that contains a <b>lpSurfMore</b> member that points to this DD_SURFACE_MORE. This handle value is also used with the D3DRENDERSTATE_TEXTUREHANDLE render state to enable texturing, and with the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DDP2OP_SETRENDERTARGET</a> and <a href="/windows-hardware/drivers/ddi/content/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DDP2OP_CLEAR</a> commands to set and clear new rendering and depth buffers. The driver should fail the call and return DDHAL_DRIVER_HANDLED if it cannot create the Direct3D surface.

For either a system memory surface or video memory surface, when <b>D3dCreateSurfaceEx</b> is called to notify about the association of <b>dwSurfaceHandle</b> with the surface's <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_global">DD_SURFACE_GLOBAL</a> and <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structures, the display driver can store any data (for example, a pointer to privately allocated memory) in the <b>dwReserved1</b> members of DD_SURFACE_GLOBAL and DD_SURFACE_LOCAL because these members are reserved for private use by the display driver. 

To notify the display driver that a system memory surface is to be released, the runtime sets the <b>fpVidMem</b> pointer member of the system memory surface's DD_SURFACE_GLOBAL structure to zero and calls the display driver's <b>D3dCreateSurfaceEx</b> callback. In addition to releasing all resources associated with this surface, the display driver must clear out the data that was previously stored in the <b>dwReserved1</b> members. Note that because the <b>fpVidMem</b> pointer member for a video memory surface can be set to zero, the display driver must verify whether the surface is in video or system memory to determine if the call to <b>D3dCreateSurfaceEx</b> is meant to notify about the association of a video memory surface with <b>dwSurfaceHandle</b> or to notify about the disassociation of a system memory surface from <b>dwSurfaceHandle</b>.

<b>D3dCreateSurfaceEx</b> is not called to notify about the disassociation of a video memory surface from <b>dwSurfaceHandle</b>; the display driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_destroysurface">DdDestroySurface</a> callback must handle local and nonlocal video memory surface deletion and must clear out data that was previously stored in the <b>dwReserved1</b> members.

The driver should also store any surface-related information that it  needs when using the surface. The driver must create a new surface table for each new <i>lpDDLcl</i> and implicitly enlarge the table when necessary to accommodate more surfaces. Typically, this is done with an exponential growth algorithm so that you do not have to enlarge the table too often. See the <i>Perm3</i> sample driver that was included with the Microsoft Windows Driver Development Kit (DDK) for implementation details. (The DDK preceded the Windows Driver Kit [WDK].)

<div class="alert"><b>Note</b>    The Microsoft Windows Driver Kit (WDK) does not contain the 3Dlabs Permedia3 (<i>Perm3.htm</i>) sample display driver. You can get this sample driver from the Windows Server 2003 SP1 DDK, which you can download from the <a href="/windows-hardware/drivers/devtest/">DDK - Windows Driver Development Kit</a> page of the WDHC website.</div>
<div> </div>
Direct3D calls <b>D3dCreateSurfaceEx</b> after the surface is created by DirectDraw by request of the Direct3D runtime or the application.

<b>D3dCreateSurfaceEx</b> can only be called with a disabled <a href="/windows-hardware/drivers/">PDEV</a> for a system memory surface. A PDEV is disabled or enabled by calling the display driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a> function. See <a href="/windows-hardware/drivers/display/managing-pdevs">Managing PDEVs</a> for more information. 

<b>Sample implementation of D3dCreateSurfaceEx</b>


```
LPDDRAWI_DDRAWSURFACE_LCL GetAttachedSurface(
    LPDDRAWI_DDRAWSURFACE_LCL pLcl,
    DDSCAPS2 * pddsCaps2)
{
    LPATTACHLIST pAl;
    pAl = pLcl->lpAttachList;
    while (pAl) {
        LPDDRAWI_DDRAWSURFACE_LCL pLclAttached = pAl->lpAttached;
        LPATTACHLIST pAlAttached = pLclAttached->lpAttachList;
        if ((pLclAttached->lpSurfMore->ddsCapsEx.dwCaps2 & pddsCaps2->dwCaps2) ||
            (pLclAttached->lpSurfMore->ddsCapsEx.dwCaps3 & pddsCaps2->dwCaps3) ||
            (pLclAttached->lpSurfMore->ddsCapsEx.dwCaps4 & pddsCaps2->dwCaps4) ||
            (pLclAttached->ddsCaps.dwCaps & pddsCaps2->dwCaps)
            )
        {
            return pLclAttached;
        }
        pAl = pAl->lpLink;
    }
    return NULL;
}
 
 
void CSExProcessPossibleMipmap(LPDDRAWI_DDRAWSURFACE_LCL pLcl)
{
    //
    // A more likely scenario would be to build a list of surfaces
    // so that the driver can create one structure that represents the
    // entire mipmap, rather than creating an object to represent each
    // level as depicted here.
    //
    DDSCAPS2 ddsCaps2 = {0,DDSCAPS2_MIPMAPSUBLEVEL,0,0};
    while (pLcl) {
        //Call the private driver routine that creates a driver-side surface structure
        CreateMyRepresentation(pLcl);
        pLcl = GetAttachedSurface(pLcl,&ddsCaps2);
    }
}

//
// The actual return type should reflect the fact that the only
// way this routine should fail is with DDERR_OUTOFMEMORY
//
void MyCreateSurfaceExHelper(LPDDRAWI_DDRAWSURFACE_LCL pLcl)
{
    LPATTACHLIST pAl;
    DDSCAPS2 ddsCaps2 = {0,0,0,0};
    LPDDRAWI_DDRAWSURFACE_LCL pLclAttached;
    LPDDRAWI_DDRAWSURFACE_LCL pLclStart;
    if (pLcl->lpGbl->fpVidMem == 0) {
        //A required check against bad surfaces
        if (pLcl->ddsCaps.dwCaps & DDSCAPS_VIDEOMEMORY)
            return;
        //Else, this is a system memory surface, so we are being informed of
        // its destruction
        DestroyMyRepresentation(pLcl->lpSurfMore->dwSurfaceHandle);
        return;
    }
    CSExProcessPossibleMipmap(pLcl);
    if (pLcl->lpSurfMore->ddsCapsEx.dwCaps2 & DDSCAPS2_CUBEMAP) {
        int i;
        //
        // The root surface is always positive X, so we check for the
        // other five face types.
        // 
        DWORD dw[5] = {
            DDSCAPS2_CUBEMAP_NEGATIVEX,
            DDSCAPS2_CUBEMAP_POSITIVEY,
            DDSCAPS2_CUBEMAP_NEGATIVEY,
            DDSCAPS2_CUBEMAP_POSITIVEZ,
            DDSCAPS2_CUBEMAP_NEGATIVEZ};
        for(i=0;i< sizeof(dw)/sizeof(dw[0]);i++) {
            ddsCaps2.dwCaps2 = dw[i];
            pLclAttached = GetAttachedSurface(pLcl, &ddsCaps2);
            if (pLclAttached)
                CSExProcessPossibleMipmap(pLclAttached);
        }
        //
        // Once we know it's a cube map, we know there cannot be any other 
        // attachments.
        //
        return; 
    }
    //
    // At this point:
    //      If it's a cubemap, we returned above.
    //      If it's a mipmap, we handled all cases above.
    // The only other complex surface possibility is a primary flipping chain.
    // Because a primary flipping chain cannot be mipmapped, we will simply return
    // here if this surface is a mipmap.
    //
    if (pLcl->ddsCaps.dwCaps & DDSCAPS_MIPMAP)
        return;
    //
    // The only system memory surfaces we'll ever be interested in are textures (mipmaps)
    // and cube maps.   We do not propagate an error code for system memory
    // surfaces whose format we do not understand. This could cause an error code to 
    // be propagated to the application when it was trying to use system memory surfaces
    // of a format we do not understand, but is valid for the reference rasterizer, for example.
    //
    if (pLcl->ddsCaps.dwCaps & DDSCAPS_SYSTEMMEMORY)
        return;
    //
    // Now walk around a flipping chain. A flipping chain is a ring of
    // surfaces attached to each other (each surface is attached to the next
    // and to the previous surface in the ring, but not to any other surface
    // in the ring).
    // We need to watch out for this circular ring and make sure we exit appropriately.
    // There is also the possibility of a z buffer attached to one of the surfaces
    // in the ring, which may or may not have been CreateSurfaceEx'ed already.
    //
    pLclStart = pLcl;
    while (pLcl && pLcl != pLclStart) {
        //Check for Z buffer attached to this surface in the ring.
        ddsCaps2.dwCaps = DDSCAPS_ZBUFFER;
        ddsCaps2.dwCaps2 = 0;
        pLclAttached = GetAttachedSurface(pLcl, &ddsCaps2);
        if (pLclAttached)
            CreateMyRepresentation(pLclAttached);
        //Check for stereo left surface attached to this surface in the ring
        ddsCaps2.dwCaps = 0;
        ddsCaps2.dwCaps2 = DDSCAPS2_STEREOSURFACELEFT;
        pLclAttached = GetAttachedSurface(pLcl, &ddsCaps2);
        if (pLclAttached)
            CreateMyRepresentation(pLclAttached);
        // Move to next surface in the primary flipping ring. The next surface is 
        // definitely in video memory (all surfaces in an attachment structure have
        // to be in the same memory type, and we excluded system memory above).
        // The next surface in the ring is thus the attached video memory surface
        // that is NOT a z buffer NOR a stereo left surface.
        ddsCaps2.dwCaps = DDSCAPS_VIDEOMEMORY;
        ddsCaps2.dwCaps2 = 0;
        do {
            pLclAttached = GetAttachedSurface(pLcl, &ddsCaps2);
        }
        while (
            pLclAttached->ddsCaps.dwCaps & DDSCAPS_ZBUFFER ||
            pLclAttached->lpSurfMore->ddsCapsEx.dwCaps2 & DDSCAPS2_STEREOSURFACELEFT
            );
        pLcl = pLclAttached;
        if (pLcl != pLclStart)
            CreateMyRepresentation(pLcl);
    }
}
```

## -see-also

<a href="/windows-hardware/drivers/ddi/content/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DDP2OP_CLEAR</a>



<a href="/windows-hardware/drivers/ddi/content/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DDP2OP_SETRENDERTARGET</a>



<a href="/windows-hardware/drivers/ddi/content/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DDP2OP_TEXBLT</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_destroyddlocal">D3dDestroyDDLocal</a>



<a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata">DD_CREATESURFACEEXDATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_global">DD_SURFACE_GLOBAL</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_more">DD_SURFACE_MORE</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_destroysurface">DdDestroySurface</a>