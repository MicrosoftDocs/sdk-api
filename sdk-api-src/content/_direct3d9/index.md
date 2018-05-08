---
UID: TP:direct3d9
ms.assetid: e1922644-f233-3eab-8912-7b4d2f26d8ec
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Direct3D 9 Graphics



Overview of the Direct3D 9 Graphics technology.

To develop Direct3D 9 Graphics, you need these headers:

 * [d3d9.h](..\d3d9\index.md)
 * [d3d9caps.h](..\d3d9caps\index.md)
 * [d3d9helper.h](..\d3d9helper\index.md)
 * [d3d9types.h](..\d3d9types\index.md)

For the programming guide, see [Direct3D 9 Graphics](https://review.docs.microsoft.com/en-us/win32-test/direct3d9).

## Functions

| Title   | Description   |
| ---- |:---- |
| [Direct3DCreate9 function](..\d3d9\nf-d3d9-direct3dcreate9.md) | Create an IDirect3D9 object and return an interface to it. |
| [Direct3DCreate9 function](..\d3d9helper\nf-d3d9helper-direct3dcreate9.md) | Create an IDirect3D9 object and return an interface to it. |
| [Direct3DCreate9Ex function](..\d3d9\nf-d3d9-direct3dcreate9ex.md) | Creates an IDirect3D9Ex object and returns an interface to it. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [D3DDISPLAYMODEEX structure](..\d3d9types\ns-d3d9types-d3ddisplaymodeex.md) | Information about the properties of a display mode. |
| [D3DDISPLAYMODEFILTER structure](..\d3d9types\ns-d3d9types-d3ddisplaymodefilter.md) | Specifies types of display modes to filter out. |
| [_D3DADAPTER_IDENTIFIER9 structure](..\d3d9types\ns-d3d9types-_d3dadapter_identifier9.md) | Contains information identifying the adapter. |
| [_D3DBOX structure](..\d3d9types\ns-d3d9types-_d3dbox.md) | Defines a volume. |
| [_D3DCAPS9 structure](..\d3d9caps\ns-d3d9caps-_d3dcaps9.md) | Represents the capabilities of the hardware exposed through the Direct3D object. |
| [_D3DCLIPSTATUS9 structure](..\d3d9types\ns-d3d9types-_d3dclipstatus9.md) | Describes the current clip status. |
| [_D3DCOLORVALUE structure](..\d3d9types\ns-d3d9types-_d3dcolorvalue.md) | Describes color values. |
| [_D3DCOMPOSERECTDESC structure](..\d3d9types\ns-d3d9types-_d3dcomposerectdesc.md) | Specifies the rectangle used to enclose glyphs on a monochrome surface. |
| [_D3DCOMPOSERECTDESTINATION structure](..\d3d9types\ns-d3d9types-_d3dcomposerectdestination.md) | Specifies the source glyph and location in a monochrome surface to copy glyphs into. |
| [_D3DDEVICE_CREATION_PARAMETERS structure](..\d3d9types\ns-d3d9types-_d3ddevice_creation_parameters.md) | Describes the creation parameters for a device. |
| [_D3DDEVINFO_D3D9BANDWIDTHTIMINGS structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_d3d9bandwidthtimings.md) | Throughput metrics for help in understanding the performance of an application. |
| [_D3DDEVINFO_D3D9CACHEUTILIZATION structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_d3d9cacheutilization.md) | Measure the cache hit rate performance for textures and indexed vertices. |
| [_D3DDEVINFO_D3D9INTERFACETIMINGS structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_d3d9interfacetimings.md) | Percent of time processing data in the driver. These statistics may help identify cases when the driver is waiting for other resources. |
| [_D3DDEVINFO_D3D9PIPELINETIMINGS structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_d3d9pipelinetimings.md) | Percent of time processing data in the pipeline. |
| [_D3DDEVINFO_D3D9STAGETIMINGS structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_d3d9stagetimings.md) | Percent of time processing shader data. |
| [_D3DDEVINFO_D3DVERTEXSTATS structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_d3dvertexstats.md) | Reports the number of triangles that have been processed and clipped by the runtime's software vertex processing. |
| [_D3DDEVINFO_RESOURCEMANAGER structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_resourcemanager.md) | Resource usage statistics. |
| [_D3DDEVINFO_VCACHE structure](..\d3d9types\ns-d3d9types-_d3ddevinfo_vcache.md) | Vertex cache optimization hints. |
| [_D3DDISPLAYMODE structure](..\d3d9types\ns-d3d9types-_d3ddisplaymode.md) | Describes the display mode. |
| [_D3DGAMMARAMP structure](..\d3d9types\ns-d3d9types-_d3dgammaramp.md) | Contains red, green, and blue ramp data. |
| [_D3DINDEXBUFFER_DESC structure](..\d3d9types\ns-d3d9types-_d3dindexbuffer_desc.md) | Describes an index buffer. |
| [_D3DLIGHT9 structure](..\d3d9types\ns-d3d9types-_d3dlight9.md) | Defines a set of lighting properties. |
| [_D3DLOCKED_BOX structure](..\d3d9types\ns-d3d9types-_d3dlocked_box.md) | Describes a locked box (volume). |
| [_D3DLOCKED_RECT structure](..\d3d9types\ns-d3d9types-_d3dlocked_rect.md) | Describes a locked rectangular region. |
| [_D3DMATERIAL9 structure](..\d3d9types\ns-d3d9types-_d3dmaterial9.md) | Specifies material properties. |
| [_D3DMEMORYPRESSURE structure](..\d3d9types\ns-d3d9types-_d3dmemorypressure.md) | Contains data for memory pressure reporting. |
| [_D3DPRESENTSTATS structure](..\d3d9types\ns-d3d9types-_d3dpresentstats.md) | Describes swapchain statistics relating to PresentEx calls. |
| [_D3DPRESENT_PARAMETERS_ structure](..\d3d9types\ns-d3d9types-_d3dpresent_parameters_.md) | Describes the presentation parameters. |
| [_D3DPSHADERCAPS2_0 structure](..\d3d9caps\ns-d3d9caps-_d3dpshadercaps2_0.md) | Pixel shader driver caps. |
| [_D3DRANGE structure](..\d3d9types\ns-d3d9types-_d3drange.md) | Defines a range. |
| [_D3DRASTER_STATUS structure](..\d3d9types\ns-d3d9types-_d3draster_status.md) | Describes the raster status. |
| [_D3DRECT structure](..\d3d9types\ns-d3d9types-_d3drect.md) | Defines a rectangle. |
| [_D3DRECTPATCH_INFO structure](..\d3d9types\ns-d3d9types-_d3drectpatch_info.md) | Describes a rectangular high-order patch. |
| [_D3DRESOURCESTATS structure](..\d3d9types\ns-d3d9types-_d3dresourcestats.md) | Resource statistics gathered by the D3DDEVINFO_ResourceManager when using the asynchronous query mechanism. |
| [_D3DSURFACE_DESC structure](..\d3d9types\ns-d3d9types-_d3dsurface_desc.md) | Describes a surface. |
| [_D3DTRIPATCH_INFO structure](..\d3d9types\ns-d3d9types-_d3dtripatch_info.md) | Describes a triangular high-order patch. |
| [_D3DVECTOR structure](..\d3d9types\ns-d3d9types-_d3dvector.md) | Defines a vector. |
| [_D3DVERTEXBUFFER_DESC structure](..\d3d9types\ns-d3d9types-_d3dvertexbuffer_desc.md) | Describes a vertex buffer. |
| [_D3DVERTEXELEMENT9 structure](..\d3d9types\ns-d3d9types-_d3dvertexelement9.md) | Defines the vertex data layout. Each vertex can contain one or more data types, and each data type is described by a vertex element. |
| [_D3DVIEWPORT9 structure](..\d3d9types\ns-d3d9types-_d3dviewport9.md) | Defines the window dimensions of a render-target surface onto which a 3D volume projects. |
| [_D3DVOLUME_DESC structure](..\d3d9types\ns-d3d9types-_d3dvolume_desc.md) | Describes a volume. |
| [_D3DVSHADERCAPS2_0 structure](..\d3d9caps\ns-d3d9caps-_d3dvshadercaps2_0.md) | Vertex shader caps. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [D3DDISPLAYROTATION enumeration](..\d3d9types\ne-d3d9types-d3ddisplayrotation.md) | Specifies how the monitor being used to display a full-screen application is rotated. |
| [D3DSCANLINEORDERING enumeration](..\d3d9types\ne-d3d9types-d3dscanlineordering.md) | Flags indicating the method the rasterizer uses to create an image on a surface. |
| [_D3DBACKBUFFER_TYPE enumeration](..\d3d9types\ne-d3d9types-_d3dbackbuffer_type.md) | Defines constants that describe the type of back buffer. |
| [_D3DBASISTYPE enumeration](..\d3d9types\ne-d3d9types-_d3dbasistype.md) | Defines the basis type of a high-order patch surface. |
| [_D3DBLEND enumeration](..\d3d9types\ne-d3d9types-_d3dblend.md) | Defines the supported blend mode. |
| [_D3DBLENDOP enumeration](..\d3d9types\ne-d3d9types-_d3dblendop.md) | Defines the supported blend operations. See Remarks for definitions of terms. |
| [_D3DCMPFUNC enumeration](..\d3d9types\ne-d3d9types-_d3dcmpfunc.md) | Defines the supported compare functions. |
| [_D3DCOMPOSERECTSOP enumeration](..\d3d9types\ne-d3d9types-_d3dcomposerectsop.md) | Specifies how to combine the glyph data from the source and destination surfaces in a call to ComposeRects. |
| [_D3DCUBEMAP_FACES enumeration](..\d3d9types\ne-d3d9types-_d3dcubemap_faces.md) | Defines the faces of a cubemap. |
| [_D3DCULL enumeration](..\d3d9types\ne-d3d9types-_d3dcull.md) | Defines the supported culling modes. |
| [_D3DDEBUGMONITORTOKENS enumeration](..\d3d9types\ne-d3d9types-_d3ddebugmonitortokens.md) | Defines the debug monitor tokens. |
| [_D3DDECLMETHOD enumeration](..\d3d9types\ne-d3d9types-_d3ddeclmethod.md) | Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation). |
| [_D3DDECLTYPE enumeration](..\d3d9types\ne-d3d9types-_d3ddecltype.md) | Defines a vertex declaration data type. |
| [_D3DDECLUSAGE enumeration](..\d3d9types\ne-d3d9types-_d3ddeclusage.md) | Identifies the intended use of vertex data. |
| [_D3DDEGREETYPE enumeration](..\d3d9types\ne-d3d9types-_d3ddegreetype.md) | Defines the degree of the variables in the equation that describes a curve. |
| [_D3DDEVTYPE enumeration](..\d3d9types\ne-d3d9types-_d3ddevtype.md) | Defines device types. |
| [_D3DFILLMODE enumeration](..\d3d9types\ne-d3d9types-_d3dfillmode.md) | Defines constants describing the fill mode. |
| [_D3DFOGMODE enumeration](..\d3d9types\ne-d3d9types-_d3dfogmode.md) | Defines constants that describe the fog mode. |
| [_D3DLIGHTTYPE enumeration](..\d3d9types\ne-d3d9types-_d3dlighttype.md) | Defines the light type. |
| [_D3DMATERIALCOLORSOURCE enumeration](..\d3d9types\ne-d3d9types-_d3dmaterialcolorsource.md) | Defines the location at which a color or color component must be accessed for lighting calculations. |
| [_D3DMULTISAMPLE_TYPE enumeration](..\d3d9types\ne-d3d9types-_d3dmultisample_type.md) | Defines the levels of full-scene multisampling that the device can apply. |
| [_D3DPATCHEDGESTYLE enumeration](..\d3d9types\ne-d3d9types-_d3dpatchedgestyle.md) | Defines whether the current tessellation mode is discrete or continuous. |
| [_D3DPOOL enumeration](..\d3d9types\ne-d3d9types-_d3dpool.md) | Defines the memory class that holds the buffers for a resource. |
| [_D3DPRIMITIVETYPE enumeration](..\d3d9types\ne-d3d9types-_d3dprimitivetype.md) | Defines the primitives supported by Direct3D. |
| [_D3DQUERYTYPE enumeration](..\d3d9types\ne-d3d9types-_d3dquerytype.md) | Identifies the query type. |
| [_D3DRENDERSTATETYPE enumeration](..\d3d9types\ne-d3d9types-_d3drenderstatetype.md) | Render states define set-up states for all kinds of vertex and pixel processing. |
| [_D3DRESOURCETYPE enumeration](..\d3d9types\ne-d3d9types-_d3dresourcetype.md) | Defines resource types. |
| [_D3DSAMPLERSTATETYPE enumeration](..\d3d9types\ne-d3d9types-_d3dsamplerstatetype.md) | Sampler states define texture sampling operations such as texture addressing and texture filtering. |
| [_D3DSAMPLER_TEXTURE_TYPE enumeration](..\d3d9types\ne-d3d9types-_d3dsampler_texture_type.md) | Defines the sampler texture types for vertex shaders. |
| [_D3DSHADEMODE enumeration](..\d3d9types\ne-d3d9types-_d3dshademode.md) | Defines constants that describe the supported shading modes. |
| [_D3DSTATEBLOCKTYPE enumeration](..\d3d9types\ne-d3d9types-_d3dstateblocktype.md) | Predefined sets of pipeline state used by state blocks (see State Blocks Save and Restore State (Direct3D 9)). |
| [_D3DSTENCILOP enumeration](..\d3d9types\ne-d3d9types-_d3dstencilop.md) | Defines stencil-buffer operations. |
| [_D3DSWAPEFFECT enumeration](..\d3d9types\ne-d3d9types-_d3dswapeffect.md) | Defines swap effects. |
| [_D3DTEXTUREADDRESS enumeration](..\d3d9types\ne-d3d9types-_d3dtextureaddress.md) | Defines constants that describe the supported texture-addressing modes. |
| [_D3DTEXTUREFILTERTYPE enumeration](..\d3d9types\ne-d3d9types-_d3dtexturefiltertype.md) | Defines texture filtering modes for a texture stage. |
| [_D3DTEXTUREOP enumeration](..\d3d9types\ne-d3d9types-_d3dtextureop.md) | Defines per-stage texture-blending operations. |
| [_D3DTEXTURESTAGESTATETYPE enumeration](..\d3d9types\ne-d3d9types-_d3dtexturestagestatetype.md) | Texture stage states define multi-blender texture operations. |
| [_D3DTEXTURETRANSFORMFLAGS enumeration](..\d3d9types\ne-d3d9types-_d3dtexturetransformflags.md) | Defines texture coordinate transformation values. |
| [_D3DTRANSFORMSTATETYPE enumeration](..\d3d9types\ne-d3d9types-_d3dtransformstatetype.md) | Defines constants that describe transformation state values. |
| [_D3DVERTEXBLENDFLAGS enumeration](..\d3d9types\ne-d3d9types-_d3dvertexblendflags.md) | Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending. |
| [_D3DZBUFFERTYPE enumeration](..\d3d9types\ne-d3d9types-_d3dzbuffertype.md) | Defines constants that describe depth-buffer formats. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDirect3D9 interface](..\d3d9\nn-d3d9-idirect3d9.md) | Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device. |
| [IDirect3D9 interface](..\d3d9helper\nn-d3d9helper-idirect3d9.md) | Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device. |
| [IDirect3D9Ex interface](..\d3d9\nn-d3d9-idirect3d9ex.md) | Applications use the methods of the IDirect3D9Ex interface (which inherits from IDirect3D9) to create Microsoft Direct3D 9Ex objects and set up the environment. |
| [IDirect3DBaseTexture9 interface](..\d3d9\nn-d3d9-idirect3dbasetexture9.md) | Applications use the methods of the IDirect3DBaseTexture9 interface to manipulate texture resources including cube and volume textures. |
| [IDirect3DBaseTexture9 interface](..\d3d9helper\nn-d3d9helper-idirect3dbasetexture9.md) | Applications use the methods of the IDirect3DBaseTexture9 interface to manipulate texture resources including cube and volume textures. |
| [IDirect3DCubeTexture9 interface](..\d3d9\nn-d3d9-idirect3dcubetexture9.md) | Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource. |
| [IDirect3DCubeTexture9 interface](..\d3d9helper\nn-d3d9helper-idirect3dcubetexture9.md) | Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource. |
| [IDirect3DDevice9 interface](..\d3d9\nn-d3d9-idirect3ddevice9.md) | Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. |
| [IDirect3DDevice9 interface](..\d3d9helper\nn-d3d9helper-idirect3ddevice9.md) | Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. |
| [IDirect3DDevice9Ex interface](..\d3d9\nn-d3d9-idirect3ddevice9ex.md) | Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. |
| [IDirect3DIndexBuffer9 interface](..\d3d9\nn-d3d9-idirect3dindexbuffer9.md) | Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource. |
| [IDirect3DIndexBuffer9 interface](..\d3d9helper\nn-d3d9helper-idirect3dindexbuffer9.md) | Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource. |
| [IDirect3DPixelShader9 interface](..\d3d9\nn-d3d9-idirect3dpixelshader9.md) | Applications use the methods of the IDirect3DPixelShader9 interface to encapsulate the functionality of a pixel shader. |
| [IDirect3DPixelShader9 interface](..\d3d9helper\nn-d3d9helper-idirect3dpixelshader9.md) | Applications use the methods of the IDirect3DPixelShader9 interface to encapsulate the functionality of a pixel shader. |
| [IDirect3DQuery9 interface](..\d3d9\nn-d3d9-idirect3dquery9.md) | Applications use the methods of the IDirect3DQuery9 interface to perform asynchronous queries on a driver. |
| [IDirect3DQuery9 interface](..\d3d9helper\nn-d3d9helper-idirect3dquery9.md) | Applications use the methods of the IDirect3DQuery9 interface to perform asynchronous queries on a driver. |
| [IDirect3DResource9 interface](..\d3d9\nn-d3d9-idirect3dresource9.md) | Applications use the methods of the IDirect3DResource9 interface to query and prepare resources. |
| [IDirect3DResource9 interface](..\d3d9helper\nn-d3d9helper-idirect3dresource9.md) | Applications use the methods of the IDirect3DResource9 interface to query and prepare resources. |
| [IDirect3DStateBlock9 interface](..\d3d9\nn-d3d9-idirect3dstateblock9.md) | Applications use the methods of the IDirect3DStateBlock9 interface to encapsulate render states. |
| [IDirect3DStateBlock9 interface](..\d3d9helper\nn-d3d9helper-idirect3dstateblock9.md) | Applications use the methods of the IDirect3DStateBlock9 interface to encapsulate render states. |
| [IDirect3DSurface9 interface](..\d3d9\nn-d3d9-idirect3dsurface9.md) | Applications use the methods of the IDirect3DSurface9 interface to query and prepare surfaces. |
| [IDirect3DSurface9 interface](..\d3d9helper\nn-d3d9helper-idirect3dsurface9.md) | Applications use the methods of the IDirect3DSurface9 interface to query and prepare surfaces. |
| [IDirect3DSwapChain9 interface](..\d3d9\nn-d3d9-idirect3dswapchain9.md) | Applications use the methods of the IDirect3DSwapChain9 interface to manipulate a swap chain. |
| [IDirect3DSwapChain9 interface](..\d3d9helper\nn-d3d9helper-idirect3dswapchain9.md) | Applications use the methods of the IDirect3DSwapChain9 interface to manipulate a swap chain. |
| [IDirect3DSwapChain9Ex interface](..\d3d9\nn-d3d9-idirect3dswapchain9ex.md) | Applications use the methods of the IDirect3DSwapChain9Ex interface to manipulate a swap chain. |
| [IDirect3DTexture9 interface](..\d3d9\nn-d3d9-idirect3dtexture9.md) | Applications use the methods of the IDirect3DTexture9 interface to manipulate a texture resource. |
| [IDirect3DTexture9 interface](..\d3d9helper\nn-d3d9helper-idirect3dtexture9.md) | Applications use the methods of the IDirect3DTexture9 interface to manipulate a texture resource. |
| [IDirect3DVertexBuffer9 interface](..\d3d9\nn-d3d9-idirect3dvertexbuffer9.md) | Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources. |
| [IDirect3DVertexBuffer9 interface](..\d3d9helper\nn-d3d9helper-idirect3dvertexbuffer9.md) | Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources. |
| [IDirect3DVertexDeclaration9 interface](..\d3d9\nn-d3d9-idirect3dvertexdeclaration9.md) | Applications use the methods of the IDirect3DVertexDeclaration9 interface to encapsulate the vertex shader declaration. |
| [IDirect3DVertexDeclaration9 interface](..\d3d9helper\nn-d3d9helper-idirect3dvertexdeclaration9.md) | Applications use the methods of the IDirect3DVertexDeclaration9 interface to encapsulate the vertex shader declaration. |
| [IDirect3DVertexShader9 interface](..\d3d9\nn-d3d9-idirect3dvertexshader9.md) | Applications use the methods of the IDirect3DVertexShader9 interface to encapsulate the functionality of a vertex shader. |
| [IDirect3DVertexShader9 interface](..\d3d9helper\nn-d3d9helper-idirect3dvertexshader9.md) | Applications use the methods of the IDirect3DVertexShader9 interface to encapsulate the functionality of a vertex shader. |
| [IDirect3DVolume9 interface](..\d3d9\nn-d3d9-idirect3dvolume9.md) | Applications use the methods of the IDirect3DVolume9 interface to manipulate volume resources. |
| [IDirect3DVolume9 interface](..\d3d9helper\nn-d3d9helper-idirect3dvolume9.md) | Applications use the methods of the IDirect3DVolume9 interface to manipulate volume resources. |
| [IDirect3DVolumeTexture9 interface](..\d3d9\nn-d3d9-idirect3dvolumetexture9.md) | Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource. |
| [IDirect3DVolumeTexture9 interface](..\d3d9helper\nn-d3d9helper-idirect3dvolumetexture9.md) | Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [D3DCOLOR_ARGB macro](..\d3d9types\nf-d3d9types-d3dcolor_argb.md) | Initializes a color with the supplied alpha, red, green, and blue values. |
| [D3DCOLOR_AYUV macro](..\d3d9types\nf-d3d9types-d3dcolor_ayuv.md) | Initializes a color using the (a,y,u,v) values. |
| [D3DCOLOR_COLORVALUE macro](..\d3d9types\nf-d3d9types-d3dcolor_colorvalue.md) | Initializes a color with the supplied red, green, blue, and alpha floating-point values. |
| [D3DCOLOR_RGBA macro](..\d3d9types\nf-d3d9types-d3dcolor_rgba.md) | Initializes a color with the supplied red, green, blue, and alpha values. |
| [D3DCOLOR_XRGB macro](..\d3d9types\nf-d3d9types-d3dcolor_xrgb.md) | Initializes a color with the supplied red, green, and blue values. |
| [D3DCOLOR_XYUV macro](..\d3d9types\nf-d3d9types-d3dcolor_xyuv.md) | Initializes a color with the (y, u, v) values. |
| [D3DPS_VERSION macro](..\d3d9types\nf-d3d9types-d3dps_version.md) | Create a pixel shader version token. |
| [D3DTS_WORLDMATRIX macro](..\d3d9types\nf-d3d9types-d3dts_worldmatrix.md) | Maps indices in the range 0 through 255 to the corresponding transform states. |
| [D3DVS_VERSION macro](..\d3d9types\nf-d3d9types-d3dvs_version.md) | Create a vertex shader version number token. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDirect3D9::CheckDepthStencilMatch](..\d3d9\nf-d3d9-idirect3d9-checkdepthstencilmatch.md) | Determines whether a depth-stencil format is compatible with a render-target format in a particular display mode. |
| [IDirect3D9::CheckDepthStencilMatch](..\d3d9helper\nf-d3d9helper-idirect3d9-checkdepthstencilmatch.md) | Determines whether a depth-stencil format is compatible with a render-target format in a particular display mode. |
| [IDirect3D9::CheckDeviceFormatConversion](..\d3d9\nf-d3d9-idirect3d9-checkdeviceformatconversion.md) | Tests the device to see if it supports conversion from one display format to another. |
| [IDirect3D9::CheckDeviceFormatConversion](..\d3d9helper\nf-d3d9helper-idirect3d9-checkdeviceformatconversion.md) | Tests the device to see if it supports conversion from one display format to another. |
| [IDirect3D9::CheckDeviceFormat](..\d3d9\nf-d3d9-idirect3d9-checkdeviceformat.md) | Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter. |
| [IDirect3D9::CheckDeviceFormat](..\d3d9helper\nf-d3d9helper-idirect3d9-checkdeviceformat.md) | Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter. |
| [IDirect3D9::CheckDeviceMultiSampleType](..\d3d9\nf-d3d9-idirect3d9-checkdevicemultisampletype.md) | Determines if a multisampling technique is available on this device. |
| [IDirect3D9::CheckDeviceMultiSampleType](..\d3d9helper\nf-d3d9helper-idirect3d9-checkdevicemultisampletype.md) | Determines if a multisampling technique is available on this device. |
| [IDirect3D9::CheckDeviceType](..\d3d9\nf-d3d9-idirect3d9-checkdevicetype.md) | Verifies whether a hardware accelerated device type can be used on this adapter. |
| [IDirect3D9::CheckDeviceType](..\d3d9helper\nf-d3d9helper-idirect3d9-checkdevicetype.md) | Verifies whether a hardware accelerated device type can be used on this adapter. |
| [IDirect3D9::CreateDevice](..\d3d9\nf-d3d9-idirect3d9-createdevice.md) | Creates a device to represent the display adapter. |
| [IDirect3D9::CreateDevice](..\d3d9helper\nf-d3d9helper-idirect3d9-createdevice.md) | Creates a device to represent the display adapter. |
| [IDirect3D9::EnumAdapterModes](..\d3d9\nf-d3d9-idirect3d9-enumadaptermodes.md) | Queries the device to determine whether the specified adapter supports the requested format and display mode. This method could be used in a loop to enumerate all the available adapter modes. |
| [IDirect3D9::EnumAdapterModes](..\d3d9helper\nf-d3d9helper-idirect3d9-enumadaptermodes.md) | Queries the device to determine whether the specified adapter supports the requested format and display mode. This method could be used in a loop to enumerate all the available adapter modes. |
| [IDirect3D9::GetAdapterCount](..\d3d9\nf-d3d9-idirect3d9-getadaptercount.md) | Returns the number of adapters on the system. |
| [IDirect3D9::GetAdapterCount](..\d3d9helper\nf-d3d9helper-idirect3d9-getadaptercount.md) | Returns the number of adapters on the system. |
| [IDirect3D9::GetAdapterDisplayMode](..\d3d9\nf-d3d9-idirect3d9-getadapterdisplaymode.md) | Retrieves the current display mode of the adapter. |
| [IDirect3D9::GetAdapterDisplayMode](..\d3d9helper\nf-d3d9helper-idirect3d9-getadapterdisplaymode.md) | Retrieves the current display mode of the adapter. |
| [IDirect3D9::GetAdapterIdentifier](..\d3d9\nf-d3d9-idirect3d9-getadapteridentifier.md) | Describes the physical display adapters present in the system when the IDirect3D9 interface was instantiated. |
| [IDirect3D9::GetAdapterIdentifier](..\d3d9helper\nf-d3d9helper-idirect3d9-getadapteridentifier.md) | Describes the physical display adapters present in the system when the IDirect3D9 interface was instantiated. |
| [IDirect3D9::GetAdapterModeCount](..\d3d9\nf-d3d9-idirect3d9-getadaptermodecount.md) | Returns the number of display modes available on this adapter. |
| [IDirect3D9::GetAdapterModeCount](..\d3d9helper\nf-d3d9helper-idirect3d9-getadaptermodecount.md) | Returns the number of display modes available on this adapter. |
| [IDirect3D9::GetAdapterMonitor](..\d3d9\nf-d3d9-idirect3d9-getadaptermonitor.md) | Returns the handle of the monitor associated with the Direct3D object. |
| [IDirect3D9::GetAdapterMonitor](..\d3d9helper\nf-d3d9helper-idirect3d9-getadaptermonitor.md) | Returns the handle of the monitor associated with the Direct3D object. |
| [IDirect3D9::GetDeviceCaps](..\d3d9\nf-d3d9-idirect3d9-getdevicecaps.md) | Retrieves device-specific information about a device. |
| [IDirect3D9::GetDeviceCaps](..\d3d9helper\nf-d3d9helper-idirect3d9-getdevicecaps.md) | Retrieves device-specific information about a device. |
| [IDirect3D9::RegisterSoftwareDevice](..\d3d9\nf-d3d9-idirect3d9-registersoftwaredevice.md) | Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers. |
| [IDirect3D9::RegisterSoftwareDevice](..\d3d9helper\nf-d3d9helper-idirect3d9-registersoftwaredevice.md) | Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers. |
| [IDirect3D9Ex::CreateDeviceEx](..\d3d9\nf-d3d9-idirect3d9ex-createdeviceex.md) | Creates a device to represent the display adapter. |
| [IDirect3D9Ex::EnumAdapterModesEx](..\d3d9\nf-d3d9-idirect3d9ex-enumadaptermodesex.md) | This method returns the actual display mode info based on the given mode index. |
| [IDirect3D9Ex::GetAdapterDisplayModeEx](..\d3d9\nf-d3d9-idirect3d9ex-getadapterdisplaymodeex.md) | Retrieves the current display mode and rotation settings of the adapter. |
| [IDirect3D9Ex::GetAdapterLUID](..\d3d9\nf-d3d9-idirect3d9ex-getadapterluid.md) | This method returns a unique identifier for the adapter that is specific to the adapter hardware. Applications can use this identifier to define robust mappings across various APIs (Direct3D 9, DXGI). |
| [IDirect3D9Ex::GetAdapterModeCountEx](..\d3d9\nf-d3d9-idirect3d9ex-getadaptermodecountex.md) | Returns the number of display modes available. |
| [IDirect3DBaseTexture9::GenerateMipSubLevels](..\d3d9\nf-d3d9-idirect3dbasetexture9-generatemipsublevels.md) | Generate mipmap sublevels. |
| [IDirect3DBaseTexture9::GenerateMipSubLevels](..\d3d9helper\nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels.md) | Generate mipmap sublevels. |
| [IDirect3DBaseTexture9::GetAutoGenFilterType](..\d3d9\nf-d3d9-idirect3dbasetexture9-getautogenfiltertype.md) | Get the filter type that is used for automatically generated mipmap sublevels. |
| [IDirect3DBaseTexture9::GetAutoGenFilterType](..\d3d9helper\nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype.md) | Get the filter type that is used for automatically generated mipmap sublevels. |
| [IDirect3DBaseTexture9::GetLOD](..\d3d9\nf-d3d9-idirect3dbasetexture9-getlod.md) | Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture). |
| [IDirect3DBaseTexture9::GetLOD](..\d3d9helper\nf-d3d9helper-idirect3dbasetexture9-getlod.md) | Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture). |
| [IDirect3DBaseTexture9::GetLevelCount](..\d3d9\nf-d3d9-idirect3dbasetexture9-getlevelcount.md) | Returns the number of texture levels in a multilevel texture. |
| [IDirect3DBaseTexture9::GetLevelCount](..\d3d9helper\nf-d3d9helper-idirect3dbasetexture9-getlevelcount.md) | Returns the number of texture levels in a multilevel texture. |
| [IDirect3DBaseTexture9::SetAutoGenFilterType](..\d3d9\nf-d3d9-idirect3dbasetexture9-setautogenfiltertype.md) | Set the filter type that is used for automatically generated mipmap sublevels. |
| [IDirect3DBaseTexture9::SetAutoGenFilterType](..\d3d9helper\nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype.md) | Set the filter type that is used for automatically generated mipmap sublevels. |
| [IDirect3DBaseTexture9::SetLOD](..\d3d9\nf-d3d9-idirect3dbasetexture9-setlod.md) | Sets the most detailed level-of-detail for a managed texture. |
| [IDirect3DBaseTexture9::SetLOD](..\d3d9helper\nf-d3d9helper-idirect3dbasetexture9-setlod.md) | Sets the most detailed level-of-detail for a managed texture. |
| [IDirect3DCubeTexture9::AddDirtyRect](..\d3d9\nf-d3d9-idirect3dcubetexture9-adddirtyrect.md) | Adds a dirty region to a cube texture resource. |
| [IDirect3DCubeTexture9::AddDirtyRect](..\d3d9helper\nf-d3d9helper-idirect3dcubetexture9-adddirtyrect.md) | Adds a dirty region to a cube texture resource. |
| [IDirect3DCubeTexture9::GetCubeMapSurface](..\d3d9\nf-d3d9-idirect3dcubetexture9-getcubemapsurface.md) | Retrieves a cube texture map surface. |
| [IDirect3DCubeTexture9::GetCubeMapSurface](..\d3d9helper\nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface.md) | Retrieves a cube texture map surface. |
| [IDirect3DCubeTexture9::GetLevelDesc](..\d3d9\nf-d3d9-idirect3dcubetexture9-getleveldesc.md) | Retrieves a description of one face of the specified cube texture level. |
| [IDirect3DCubeTexture9::GetLevelDesc](..\d3d9helper\nf-d3d9helper-idirect3dcubetexture9-getleveldesc.md) | Retrieves a description of one face of the specified cube texture level. |
| [IDirect3DCubeTexture9::LockRect](..\d3d9\nf-d3d9-idirect3dcubetexture9-lockrect.md) | Locks a rectangle on a cube texture resource. |
| [IDirect3DCubeTexture9::LockRect](..\d3d9helper\nf-d3d9helper-idirect3dcubetexture9-lockrect.md) | Locks a rectangle on a cube texture resource. |
| [IDirect3DCubeTexture9::UnlockRect](..\d3d9\nf-d3d9-idirect3dcubetexture9-unlockrect.md) | Unlocks a rectangle on a cube texture resource. |
| [IDirect3DCubeTexture9::UnlockRect](..\d3d9helper\nf-d3d9helper-idirect3dcubetexture9-unlockrect.md) | Unlocks a rectangle on a cube texture resource. |
| [IDirect3DDevice9::BeginScene](..\d3d9\nf-d3d9-idirect3ddevice9-beginscene.md) | Begins a scene. |
| [IDirect3DDevice9::BeginScene](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-beginscene.md) | Begins a scene. |
| [IDirect3DDevice9::BeginStateBlock](..\d3d9\nf-d3d9-idirect3ddevice9-beginstateblock.md) | Signals Direct3D to begin recording a device-state block. |
| [IDirect3DDevice9::BeginStateBlock](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-beginstateblock.md) | Signals Direct3D to begin recording a device-state block. |
| [IDirect3DDevice9::Clear](..\d3d9\nf-d3d9-idirect3ddevice9-clear.md) | Clears one or more surfaces such as a render target, multiple render targets, a stencil buffer, and a depth buffer. |
| [IDirect3DDevice9::Clear](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-clear.md) | Clears one or more surfaces such as a render target, multiple render targets, a stencil buffer, and a depth buffer. |
| [IDirect3DDevice9::ColorFill](..\d3d9\nf-d3d9-idirect3ddevice9-colorfill.md) | Allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color. |
| [IDirect3DDevice9::ColorFill](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-colorfill.md) | Allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color. |
| [IDirect3DDevice9::CreateAdditionalSwapChain](..\d3d9\nf-d3d9-idirect3ddevice9-createadditionalswapchain.md) | Creates an additional swap chain for rendering multiple views. |
| [IDirect3DDevice9::CreateAdditionalSwapChain](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createadditionalswapchain.md) | Creates an additional swap chain for rendering multiple views. |
| [IDirect3DDevice9::CreateCubeTexture](..\d3d9\nf-d3d9-idirect3ddevice9-createcubetexture.md) | Creates a cube texture resource. |
| [IDirect3DDevice9::CreateCubeTexture](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createcubetexture.md) | Creates a cube texture resource. |
| [IDirect3DDevice9::CreateDepthStencilSurface](..\d3d9\nf-d3d9-idirect3ddevice9-createdepthstencilsurface.md) | Creates a depth-stencil resource. |
| [IDirect3DDevice9::CreateDepthStencilSurface](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface.md) | Creates a depth-stencil resource. |
| [IDirect3DDevice9::CreateIndexBuffer](..\d3d9\nf-d3d9-idirect3ddevice9-createindexbuffer.md) | Creates an index buffer. |
| [IDirect3DDevice9::CreateIndexBuffer](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createindexbuffer.md) | Creates an index buffer. |
| [IDirect3DDevice9::CreateOffscreenPlainSurface](..\d3d9\nf-d3d9-idirect3ddevice9-createoffscreenplainsurface.md) | Create an off-screen surface. |
| [IDirect3DDevice9::CreateOffscreenPlainSurface](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface.md) | Create an off-screen surface. |
| [IDirect3DDevice9::CreatePixelShader](..\d3d9\nf-d3d9-idirect3ddevice9-createpixelshader.md) | Creates a pixel shader. |
| [IDirect3DDevice9::CreatePixelShader](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createpixelshader.md) | Creates a pixel shader. |
| [IDirect3DDevice9::CreateQuery](..\d3d9\nf-d3d9-idirect3ddevice9-createquery.md) | Creates a status query. |
| [IDirect3DDevice9::CreateQuery](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createquery.md) | Creates a status query. |
| [IDirect3DDevice9::CreateRenderTarget](..\d3d9\nf-d3d9-idirect3ddevice9-createrendertarget.md) | Creates a render-target surface. |
| [IDirect3DDevice9::CreateRenderTarget](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createrendertarget.md) | Creates a render-target surface. |
| [IDirect3DDevice9::CreateStateBlock](..\d3d9\nf-d3d9-idirect3ddevice9-createstateblock.md) | Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states. |
| [IDirect3DDevice9::CreateStateBlock](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createstateblock.md) | Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states. |
| [IDirect3DDevice9::CreateTexture](..\d3d9\nf-d3d9-idirect3ddevice9-createtexture.md) | Creates a texture resource. |
| [IDirect3DDevice9::CreateTexture](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createtexture.md) | Creates a texture resource. |
| [IDirect3DDevice9::CreateVertexBuffer](..\d3d9\nf-d3d9-idirect3ddevice9-createvertexbuffer.md) | Creates a vertex buffer. |
| [IDirect3DDevice9::CreateVertexBuffer](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createvertexbuffer.md) | Creates a vertex buffer. |
| [IDirect3DDevice9::CreateVertexDeclaration](..\d3d9\nf-d3d9-idirect3ddevice9-createvertexdeclaration.md) | Create a vertex shader declaration from the device and the vertex elements. |
| [IDirect3DDevice9::CreateVertexDeclaration](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createvertexdeclaration.md) | Create a vertex shader declaration from the device and the vertex elements. |
| [IDirect3DDevice9::CreateVertexShader](..\d3d9\nf-d3d9-idirect3ddevice9-createvertexshader.md) | Creates a vertex shader. |
| [IDirect3DDevice9::CreateVertexShader](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createvertexshader.md) | Creates a vertex shader. |
| [IDirect3DDevice9::CreateVolumeTexture](..\d3d9\nf-d3d9-idirect3ddevice9-createvolumetexture.md) | Creates a volume texture resource. |
| [IDirect3DDevice9::CreateVolumeTexture](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-createvolumetexture.md) | Creates a volume texture resource. |
| [IDirect3DDevice9::DeletePatch](..\d3d9\nf-d3d9-idirect3ddevice9-deletepatch.md) | Frees a cached high-order patch. |
| [IDirect3DDevice9::DeletePatch](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-deletepatch.md) | Frees a cached high-order patch. |
| [IDirect3DDevice9::DrawIndexedPrimitiveUP](..\d3d9\nf-d3d9-idirect3ddevice9-drawindexedprimitiveup.md) | Renders the specified geometric primitive with data specified by a user memory pointer. |
| [IDirect3DDevice9::DrawIndexedPrimitiveUP](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup.md) | Renders the specified geometric primitive with data specified by a user memory pointer. |
| [IDirect3DDevice9::DrawIndexedPrimitive](..\d3d9\nf-d3d9-idirect3ddevice9-drawindexedprimitive.md) | Based on indexing, renders the specified geometric primitive into an array of vertices. |
| [IDirect3DDevice9::DrawIndexedPrimitive](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-drawindexedprimitive.md) | Based on indexing, renders the specified geometric primitive into an array of vertices. |
| [IDirect3DDevice9::DrawPrimitiveUP](..\d3d9\nf-d3d9-idirect3ddevice9-drawprimitiveup.md) | Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type. |
| [IDirect3DDevice9::DrawPrimitiveUP](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-drawprimitiveup.md) | Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type. |
| [IDirect3DDevice9::DrawPrimitive](..\d3d9\nf-d3d9-idirect3ddevice9-drawprimitive.md) | Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams. |
| [IDirect3DDevice9::DrawPrimitive](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-drawprimitive.md) | Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams. |
| [IDirect3DDevice9::DrawRectPatch](..\d3d9\nf-d3d9-idirect3ddevice9-drawrectpatch.md) | Draws a rectangular patch using the currently set streams. |
| [IDirect3DDevice9::DrawRectPatch](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-drawrectpatch.md) | Draws a rectangular patch using the currently set streams. |
| [IDirect3DDevice9::DrawTriPatch](..\d3d9\nf-d3d9-idirect3ddevice9-drawtripatch.md) | Draws a triangular patch using the currently set streams. |
| [IDirect3DDevice9::DrawTriPatch](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-drawtripatch.md) | Draws a triangular patch using the currently set streams. |
| [IDirect3DDevice9::EndScene](..\d3d9\nf-d3d9-idirect3ddevice9-endscene.md) | Ends a scene that was begun by calling IDirect3DDevice9 |
| [IDirect3DDevice9::EndScene](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-endscene.md) | Ends a scene that was begun by calling IDirect3DDevice9 |
| [IDirect3DDevice9::EndStateBlock](..\d3d9\nf-d3d9-idirect3ddevice9-endstateblock.md) | Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface. |
| [IDirect3DDevice9::EndStateBlock](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-endstateblock.md) | Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface. |
| [IDirect3DDevice9::EvictManagedResources](..\d3d9\nf-d3d9-idirect3ddevice9-evictmanagedresources.md) | Evicts all managed resources, including both Direct3D and driver-managed resources. |
| [IDirect3DDevice9::EvictManagedResources](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-evictmanagedresources.md) | Evicts all managed resources, including both Direct3D and driver-managed resources. |
| [IDirect3DDevice9::GetAvailableTextureMem](..\d3d9\nf-d3d9-idirect3ddevice9-getavailabletexturemem.md) | Returns an estimate of the amount of available texture memory. |
| [IDirect3DDevice9::GetAvailableTextureMem](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getavailabletexturemem.md) | Returns an estimate of the amount of available texture memory. |
| [IDirect3DDevice9::GetBackBuffer](..\d3d9\nf-d3d9-idirect3ddevice9-getbackbuffer.md) | Retrieves a back buffer from the device's swap chain. |
| [IDirect3DDevice9::GetBackBuffer](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getbackbuffer.md) | Retrieves a back buffer from the device's swap chain. |
| [IDirect3DDevice9::GetClipPlane](..\d3d9\nf-d3d9-idirect3ddevice9-getclipplane.md) | Retrieves the coefficients of a user-defined clipping plane for the device. |
| [IDirect3DDevice9::GetClipPlane](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getclipplane.md) | Retrieves the coefficients of a user-defined clipping plane for the device. |
| [IDirect3DDevice9::GetClipStatus](..\d3d9\nf-d3d9-idirect3ddevice9-getclipstatus.md) | Retrieves the clip status. |
| [IDirect3DDevice9::GetClipStatus](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getclipstatus.md) | Retrieves the clip status. |
| [IDirect3DDevice9::GetCreationParameters](..\d3d9\nf-d3d9-idirect3ddevice9-getcreationparameters.md) | Retrieves the creation parameters of the device. |
| [IDirect3DDevice9::GetCreationParameters](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getcreationparameters.md) | Retrieves the creation parameters of the device. |
| [IDirect3DDevice9::GetCurrentTexturePalette](..\d3d9\nf-d3d9-idirect3ddevice9-getcurrenttexturepalette.md) | Retrieves the current texture palette. |
| [IDirect3DDevice9::GetCurrentTexturePalette](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getcurrenttexturepalette.md) | Retrieves the current texture palette. |
| [IDirect3DDevice9::GetDepthStencilSurface](..\d3d9\nf-d3d9-idirect3ddevice9-getdepthstencilsurface.md) | Gets the depth-stencil surface owned by the Direct3DDevice object. |
| [IDirect3DDevice9::GetDepthStencilSurface](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface.md) | Gets the depth-stencil surface owned by the Direct3DDevice object. |
| [IDirect3DDevice9::GetDeviceCaps](..\d3d9\nf-d3d9-idirect3ddevice9-getdevicecaps.md) | Retrieves the capabilities of the rendering device. |
| [IDirect3DDevice9::GetDeviceCaps](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getdevicecaps.md) | Retrieves the capabilities of the rendering device. |
| [IDirect3DDevice9::GetDirect3D](..\d3d9\nf-d3d9-idirect3ddevice9-getdirect3d.md) | Returns an interface to the instance of the Direct3D object that created the device. |
| [IDirect3DDevice9::GetDirect3D](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getdirect3d.md) | Returns an interface to the instance of the Direct3D object that created the device. |
| [IDirect3DDevice9::GetDisplayMode](..\d3d9\nf-d3d9-idirect3ddevice9-getdisplaymode.md) | Retrieves the display mode's spatial resolution, color resolution, and refresh frequency. |
| [IDirect3DDevice9::GetDisplayMode](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getdisplaymode.md) | Retrieves the display mode's spatial resolution, color resolution, and refresh frequency. |
| [IDirect3DDevice9::GetFVF](..\d3d9\nf-d3d9-idirect3ddevice9-getfvf.md) | Gets the fixed vertex function declaration. |
| [IDirect3DDevice9::GetFVF](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getfvf.md) | Gets the fixed vertex function declaration. |
| [IDirect3DDevice9::GetFrontBufferData](..\d3d9\nf-d3d9-idirect3ddevice9-getfrontbufferdata.md) | Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application. |
| [IDirect3DDevice9::GetFrontBufferData](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getfrontbufferdata.md) | Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application. |
| [IDirect3DDevice9::GetGammaRamp](..\d3d9\nf-d3d9-idirect3ddevice9-getgammaramp.md) | Retrieves the gamma correction ramp for the swap chain. |
| [IDirect3DDevice9::GetGammaRamp](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getgammaramp.md) | Retrieves the gamma correction ramp for the swap chain. |
| [IDirect3DDevice9::GetIndices](..\d3d9\nf-d3d9-idirect3ddevice9-getindices.md) | Retrieves index data. |
| [IDirect3DDevice9::GetIndices](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getindices.md) | Retrieves index data. |
| [IDirect3DDevice9::GetLightEnable](..\d3d9\nf-d3d9-idirect3ddevice9-getlightenable.md) | Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device. |
| [IDirect3DDevice9::GetLightEnable](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getlightenable.md) | Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device. |
| [IDirect3DDevice9::GetLight](..\d3d9\nf-d3d9-idirect3ddevice9-getlight.md) | Retrieves a set of lighting properties that this device uses. |
| [IDirect3DDevice9::GetLight](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getlight.md) | Retrieves a set of lighting properties that this device uses. |
| [IDirect3DDevice9::GetMaterial](..\d3d9\nf-d3d9-idirect3ddevice9-getmaterial.md) | Retrieves the current material properties for the device. |
| [IDirect3DDevice9::GetMaterial](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getmaterial.md) | Retrieves the current material properties for the device. |
| [IDirect3DDevice9::GetNPatchMode](..\d3d9\nf-d3d9-idirect3ddevice9-getnpatchmode.md) | Gets the N-patch mode segments. |
| [IDirect3DDevice9::GetNPatchMode](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getnpatchmode.md) | Gets the N-patch mode segments. |
| [IDirect3DDevice9::GetNumberOfSwapChains](..\d3d9\nf-d3d9-idirect3ddevice9-getnumberofswapchains.md) | Gets the number of implicit swap chains. |
| [IDirect3DDevice9::GetNumberOfSwapChains](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getnumberofswapchains.md) | Gets the number of implicit swap chains. |
| [IDirect3DDevice9::GetPaletteEntries](..\d3d9\nf-d3d9-idirect3ddevice9-getpaletteentries.md) | Retrieves palette entries. |
| [IDirect3DDevice9::GetPaletteEntries](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getpaletteentries.md) | Retrieves palette entries. |
| [IDirect3DDevice9::GetPixelShaderConstantB](..\d3d9\nf-d3d9-idirect3ddevice9-getpixelshaderconstantb.md) | Gets a Boolean shader constant. |
| [IDirect3DDevice9::GetPixelShaderConstantB](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb.md) | Gets a Boolean shader constant. |
| [IDirect3DDevice9::GetPixelShaderConstantF](..\d3d9\nf-d3d9-idirect3ddevice9-getpixelshaderconstantf.md) | Gets a floating-point shader constant. |
| [IDirect3DDevice9::GetPixelShaderConstantF](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf.md) | Gets a floating-point shader constant. |
| [IDirect3DDevice9::GetPixelShaderConstantI](..\d3d9\nf-d3d9-idirect3ddevice9-getpixelshaderconstanti.md) | Gets an integer shader constant. |
| [IDirect3DDevice9::GetPixelShaderConstantI](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti.md) | Gets an integer shader constant. |
| [IDirect3DDevice9::GetPixelShader](..\d3d9\nf-d3d9-idirect3ddevice9-getpixelshader.md) | Retrieves the currently set pixel shader. |
| [IDirect3DDevice9::GetPixelShader](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getpixelshader.md) | Retrieves the currently set pixel shader. |
| [IDirect3DDevice9::GetRasterStatus](..\d3d9\nf-d3d9-idirect3ddevice9-getrasterstatus.md) | Returns information describing the raster of the monitor on which the swap chain is presented. |
| [IDirect3DDevice9::GetRasterStatus](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getrasterstatus.md) | Returns information describing the raster of the monitor on which the swap chain is presented. |
| [IDirect3DDevice9::GetRenderState](..\d3d9\nf-d3d9-idirect3ddevice9-getrenderstate.md) | Retrieves a render-state value for a device. |
| [IDirect3DDevice9::GetRenderState](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getrenderstate.md) | Retrieves a render-state value for a device. |
| [IDirect3DDevice9::GetRenderTargetData](..\d3d9\nf-d3d9-idirect3ddevice9-getrendertargetdata.md) | Copies the render-target data from device memory to system memory. |
| [IDirect3DDevice9::GetRenderTargetData](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getrendertargetdata.md) | Copies the render-target data from device memory to system memory. |
| [IDirect3DDevice9::GetRenderTarget](..\d3d9\nf-d3d9-idirect3ddevice9-getrendertarget.md) | Retrieves a render-target surface. |
| [IDirect3DDevice9::GetRenderTarget](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getrendertarget.md) | Retrieves a render-target surface. |
| [IDirect3DDevice9::GetSamplerState](..\d3d9\nf-d3d9-idirect3ddevice9-getsamplerstate.md) | Gets the sampler state value. |
| [IDirect3DDevice9::GetSamplerState](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getsamplerstate.md) | Gets the sampler state value. |
| [IDirect3DDevice9::GetScissorRect](..\d3d9\nf-d3d9-idirect3ddevice9-getscissorrect.md) | Gets the scissor rectangle. |
| [IDirect3DDevice9::GetScissorRect](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getscissorrect.md) | Gets the scissor rectangle. |
| [IDirect3DDevice9::GetSoftwareVertexProcessing](..\d3d9\nf-d3d9-idirect3ddevice9-getsoftwarevertexprocessing.md) | Gets the vertex processing (hardware or software) mode. |
| [IDirect3DDevice9::GetSoftwareVertexProcessing](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getsoftwarevertexprocessing.md) | Gets the vertex processing (hardware or software) mode. |
| [IDirect3DDevice9::GetStreamSourceFreq](..\d3d9\nf-d3d9-idirect3ddevice9-getstreamsourcefreq.md) | Gets the stream source frequency divider value. |
| [IDirect3DDevice9::GetStreamSourceFreq](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getstreamsourcefreq.md) | Gets the stream source frequency divider value. |
| [IDirect3DDevice9::GetStreamSource](..\d3d9\nf-d3d9-idirect3ddevice9-getstreamsource.md) | Retrieves a vertex buffer bound to the specified data stream. |
| [IDirect3DDevice9::GetStreamSource](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getstreamsource.md) | Retrieves a vertex buffer bound to the specified data stream. |
| [IDirect3DDevice9::GetSwapChain](..\d3d9\nf-d3d9-idirect3ddevice9-getswapchain.md) | Gets a pointer to a swap chain. |
| [IDirect3DDevice9::GetSwapChain](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getswapchain.md) | Gets a pointer to a swap chain. |
| [IDirect3DDevice9::GetTextureStageState](..\d3d9\nf-d3d9-idirect3ddevice9-gettexturestagestate.md) | Retrieves a state value for an assigned texture. |
| [IDirect3DDevice9::GetTextureStageState](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-gettexturestagestate.md) | Retrieves a state value for an assigned texture. |
| [IDirect3DDevice9::GetTexture](..\d3d9\nf-d3d9-idirect3ddevice9-gettexture.md) | Retrieves a texture assigned to a stage for a device. |
| [IDirect3DDevice9::GetTexture](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-gettexture.md) | Retrieves a texture assigned to a stage for a device. |
| [IDirect3DDevice9::GetTransform](..\d3d9\nf-d3d9-idirect3ddevice9-gettransform.md) | Retrieves a matrix describing a transformation state. |
| [IDirect3DDevice9::GetTransform](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-gettransform.md) | Retrieves a matrix describing a transformation state. |
| [IDirect3DDevice9::GetVertexDeclaration](..\d3d9\nf-d3d9-idirect3ddevice9-getvertexdeclaration.md) | Gets a vertex shader declaration. |
| [IDirect3DDevice9::GetVertexDeclaration](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getvertexdeclaration.md) | Gets a vertex shader declaration. |
| [IDirect3DDevice9::GetVertexShaderConstantB](..\d3d9\nf-d3d9-idirect3ddevice9-getvertexshaderconstantb.md) | Gets a Boolean vertex shader constant. |
| [IDirect3DDevice9::GetVertexShaderConstantB](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getvertexshaderconstantb.md) | Gets a Boolean vertex shader constant. |
| [IDirect3DDevice9::GetVertexShaderConstantF](..\d3d9\nf-d3d9-idirect3ddevice9-getvertexshaderconstantf.md) | Gets a floating-point vertex shader constant. |
| [IDirect3DDevice9::GetVertexShaderConstantF](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getvertexshaderconstantf.md) | Gets a floating-point vertex shader constant. |
| [IDirect3DDevice9::GetVertexShaderConstantI](..\d3d9\nf-d3d9-idirect3ddevice9-getvertexshaderconstanti.md) | Gets an integer vertex shader constant. |
| [IDirect3DDevice9::GetVertexShaderConstantI](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getvertexshaderconstanti.md) | Gets an integer vertex shader constant. |
| [IDirect3DDevice9::GetVertexShader](..\d3d9\nf-d3d9-idirect3ddevice9-getvertexshader.md) | Retrieves the currently set vertex shader. |
| [IDirect3DDevice9::GetVertexShader](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getvertexshader.md) | Retrieves the currently set vertex shader. |
| [IDirect3DDevice9::GetViewport](..\d3d9\nf-d3d9-idirect3ddevice9-getviewport.md) | Retrieves the viewport parameters currently set for the device. |
| [IDirect3DDevice9::GetViewport](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-getviewport.md) | Retrieves the viewport parameters currently set for the device. |
| [IDirect3DDevice9::LightEnable](..\d3d9\nf-d3d9-idirect3ddevice9-lightenable.md) | Enables or disables a set of lighting parameters within a device. |
| [IDirect3DDevice9::LightEnable](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-lightenable.md) | Enables or disables a set of lighting parameters within a device. |
| [IDirect3DDevice9::MultiplyTransform](..\d3d9\nf-d3d9-idirect3ddevice9-multiplytransform.md) | Multiplies a device's world, view, or projection matrices by a specified matrix. |
| [IDirect3DDevice9::MultiplyTransform](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-multiplytransform.md) | Multiplies a device's world, view, or projection matrices by a specified matrix. |
| [IDirect3DDevice9::Present](..\d3d9\nf-d3d9-idirect3ddevice9-present.md) | Presents the contents of the next buffer in the sequence of back buffers owned by the device. |
| [IDirect3DDevice9::Present](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-present.md) | Presents the contents of the next buffer in the sequence of back buffers owned by the device. |
| [IDirect3DDevice9::ProcessVertices](..\d3d9\nf-d3d9-idirect3ddevice9-processvertices.md) | Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer. |
| [IDirect3DDevice9::ProcessVertices](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-processvertices.md) | Applies the vertex processing defined by the vertex shader to the set of input data streams, generating a single stream of interleaved vertex data to the destination vertex buffer. |
| [IDirect3DDevice9::Reset](..\d3d9\nf-d3d9-idirect3ddevice9-reset.md) | Resets the type, size, and format of the swap chain. |
| [IDirect3DDevice9::Reset](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-reset.md) | Resets the type, size, and format of the swap chain. |
| [IDirect3DDevice9::SetClipPlane](..\d3d9\nf-d3d9-idirect3ddevice9-setclipplane.md) | Sets the coefficients of a user-defined clipping plane for the device. |
| [IDirect3DDevice9::SetClipPlane](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setclipplane.md) | Sets the coefficients of a user-defined clipping plane for the device. |
| [IDirect3DDevice9::SetClipStatus](..\d3d9\nf-d3d9-idirect3ddevice9-setclipstatus.md) | Sets the clip status. |
| [IDirect3DDevice9::SetClipStatus](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setclipstatus.md) | Sets the clip status. |
| [IDirect3DDevice9::SetCurrentTexturePalette](..\d3d9\nf-d3d9-idirect3ddevice9-setcurrenttexturepalette.md) | Sets the current texture palette. |
| [IDirect3DDevice9::SetCurrentTexturePalette](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setcurrenttexturepalette.md) | Sets the current texture palette. |
| [IDirect3DDevice9::SetCursorPosition](..\d3d9\nf-d3d9-idirect3ddevice9-setcursorposition.md) | Sets the cursor position and update options. |
| [IDirect3DDevice9::SetCursorPosition](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setcursorposition.md) | Sets the cursor position and update options. |
| [IDirect3DDevice9::SetCursorProperties](..\d3d9\nf-d3d9-idirect3ddevice9-setcursorproperties.md) | Sets properties for the cursor. |
| [IDirect3DDevice9::SetCursorProperties](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setcursorproperties.md) | Sets properties for the cursor. |
| [IDirect3DDevice9::SetDepthStencilSurface](..\d3d9\nf-d3d9-idirect3ddevice9-setdepthstencilsurface.md) | Sets the depth stencil surface. |
| [IDirect3DDevice9::SetDepthStencilSurface](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface.md) | Sets the depth stencil surface. |
| [IDirect3DDevice9::SetDialogBoxMode](..\d3d9\nf-d3d9-idirect3ddevice9-setdialogboxmode.md) | This method allows the use of GDI dialog boxes in full-screen mode applications. |
| [IDirect3DDevice9::SetDialogBoxMode](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setdialogboxmode.md) | This method allows the use of GDI dialog boxes in full-screen mode applications. |
| [IDirect3DDevice9::SetFVF](..\d3d9\nf-d3d9-idirect3ddevice9-setfvf.md) | Sets the current vertex stream declaration. |
| [IDirect3DDevice9::SetFVF](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setfvf.md) | Sets the current vertex stream declaration. |
| [IDirect3DDevice9::SetGammaRamp](..\d3d9\nf-d3d9-idirect3ddevice9-setgammaramp.md) | Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode). |
| [IDirect3DDevice9::SetGammaRamp](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setgammaramp.md) | Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode). |
| [IDirect3DDevice9::SetIndices](..\d3d9\nf-d3d9-idirect3ddevice9-setindices.md) | Sets index data. |
| [IDirect3DDevice9::SetIndices](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setindices.md) | Sets index data. |
| [IDirect3DDevice9::SetLight](..\d3d9\nf-d3d9-idirect3ddevice9-setlight.md) | Assigns a set of lighting properties for this device. |
| [IDirect3DDevice9::SetLight](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setlight.md) | Assigns a set of lighting properties for this device. |
| [IDirect3DDevice9::SetMaterial](..\d3d9\nf-d3d9-idirect3ddevice9-setmaterial.md) | Sets the material properties for the device. |
| [IDirect3DDevice9::SetMaterial](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setmaterial.md) | Sets the material properties for the device. |
| [IDirect3DDevice9::SetNPatchMode](..\d3d9\nf-d3d9-idirect3ddevice9-setnpatchmode.md) | Enable or disable N-patches. |
| [IDirect3DDevice9::SetNPatchMode](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setnpatchmode.md) | Enable or disable N-patches. |
| [IDirect3DDevice9::SetPaletteEntries](..\d3d9\nf-d3d9-idirect3ddevice9-setpaletteentries.md) | Sets palette entries. |
| [IDirect3DDevice9::SetPaletteEntries](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setpaletteentries.md) | Sets palette entries. |
| [IDirect3DDevice9::SetPixelShaderConstantB](..\d3d9\nf-d3d9-idirect3ddevice9-setpixelshaderconstantb.md) | Sets a Boolean shader constant. |
| [IDirect3DDevice9::SetPixelShaderConstantB](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb.md) | Sets a Boolean shader constant. |
| [IDirect3DDevice9::SetPixelShaderConstantF](..\d3d9\nf-d3d9-idirect3ddevice9-setpixelshaderconstantf.md) | Sets a floating-point shader constant. |
| [IDirect3DDevice9::SetPixelShaderConstantF](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf.md) | Sets a floating-point shader constant. |
| [IDirect3DDevice9::SetPixelShaderConstantI](..\d3d9\nf-d3d9-idirect3ddevice9-setpixelshaderconstanti.md) | Sets an integer shader constant. |
| [IDirect3DDevice9::SetPixelShaderConstantI](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti.md) | Sets an integer shader constant. |
| [IDirect3DDevice9::SetPixelShader](..\d3d9\nf-d3d9-idirect3ddevice9-setpixelshader.md) | Sets the current pixel shader to a previously created pixel shader. |
| [IDirect3DDevice9::SetPixelShader](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setpixelshader.md) | Sets the current pixel shader to a previously created pixel shader. |
| [IDirect3DDevice9::SetRenderState](..\d3d9\nf-d3d9-idirect3ddevice9-setrenderstate.md) | Sets a single device render-state parameter. |
| [IDirect3DDevice9::SetRenderState](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setrenderstate.md) | Sets a single device render-state parameter. |
| [IDirect3DDevice9::SetRenderTarget](..\d3d9\nf-d3d9-idirect3ddevice9-setrendertarget.md) | Sets a new color buffer for the device. |
| [IDirect3DDevice9::SetRenderTarget](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setrendertarget.md) | Sets a new color buffer for the device. |
| [IDirect3DDevice9::SetSamplerState](..\d3d9\nf-d3d9-idirect3ddevice9-setsamplerstate.md) | Sets the sampler state value. |
| [IDirect3DDevice9::SetSamplerState](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setsamplerstate.md) | Sets the sampler state value. |
| [IDirect3DDevice9::SetScissorRect](..\d3d9\nf-d3d9-idirect3ddevice9-setscissorrect.md) | Sets the scissor rectangle. |
| [IDirect3DDevice9::SetScissorRect](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setscissorrect.md) | Sets the scissor rectangle. |
| [IDirect3DDevice9::SetSoftwareVertexProcessing](..\d3d9\nf-d3d9-idirect3ddevice9-setsoftwarevertexprocessing.md) | Use this method to switch between software and hardware vertex processing. |
| [IDirect3DDevice9::SetSoftwareVertexProcessing](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing.md) | Use this method to switch between software and hardware vertex processing. |
| [IDirect3DDevice9::SetStreamSourceFreq](..\d3d9\nf-d3d9-idirect3ddevice9-setstreamsourcefreq.md) | Sets the stream source frequency divider value. This may be used to draw several instances of geometry. |
| [IDirect3DDevice9::SetStreamSourceFreq](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq.md) | Sets the stream source frequency divider value. This may be used to draw several instances of geometry. |
| [IDirect3DDevice9::SetStreamSource](..\d3d9\nf-d3d9-idirect3ddevice9-setstreamsource.md) | Binds a vertex buffer to a device data stream. For more information, see Setting the Stream Source (Direct3D 9). |
| [IDirect3DDevice9::SetStreamSource](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setstreamsource.md) | Binds a vertex buffer to a device data stream. For more information, see Setting the Stream Source (Direct3D 9). |
| [IDirect3DDevice9::SetTextureStageState](..\d3d9\nf-d3d9-idirect3ddevice9-settexturestagestate.md) | Sets the state value for the currently assigned texture. |
| [IDirect3DDevice9::SetTextureStageState](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-settexturestagestate.md) | Sets the state value for the currently assigned texture. |
| [IDirect3DDevice9::SetTexture](..\d3d9\nf-d3d9-idirect3ddevice9-settexture.md) | Assigns a texture to a stage for a device. |
| [IDirect3DDevice9::SetTexture](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-settexture.md) | Assigns a texture to a stage for a device. |
| [IDirect3DDevice9::SetTransform](..\d3d9\nf-d3d9-idirect3ddevice9-settransform.md) | Sets a single device transformation-related state. |
| [IDirect3DDevice9::SetTransform](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-settransform.md) | Sets a single device transformation-related state. |
| [IDirect3DDevice9::SetVertexDeclaration](..\d3d9\nf-d3d9-idirect3ddevice9-setvertexdeclaration.md) | Sets a Vertex Declaration (Direct3D 9). |
| [IDirect3DDevice9::SetVertexDeclaration](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setvertexdeclaration.md) | Sets a Vertex Declaration (Direct3D 9). |
| [IDirect3DDevice9::SetVertexShaderConstantB](..\d3d9\nf-d3d9-idirect3ddevice9-setvertexshaderconstantb.md) | Sets a Boolean vertex shader constant. |
| [IDirect3DDevice9::SetVertexShaderConstantB](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb.md) | Sets a Boolean vertex shader constant. |
| [IDirect3DDevice9::SetVertexShaderConstantF](..\d3d9\nf-d3d9-idirect3ddevice9-setvertexshaderconstantf.md) | Sets a floating-point vertex shader constant. |
| [IDirect3DDevice9::SetVertexShaderConstantF](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf.md) | Sets a floating-point vertex shader constant. |
| [IDirect3DDevice9::SetVertexShaderConstantI](..\d3d9\nf-d3d9-idirect3ddevice9-setvertexshaderconstanti.md) | Sets an integer vertex shader constant. |
| [IDirect3DDevice9::SetVertexShaderConstantI](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti.md) | Sets an integer vertex shader constant. |
| [IDirect3DDevice9::SetVertexShader](..\d3d9\nf-d3d9-idirect3ddevice9-setvertexshader.md) | Sets the vertex shader. |
| [IDirect3DDevice9::SetVertexShader](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setvertexshader.md) | Sets the vertex shader. |
| [IDirect3DDevice9::SetViewport](..\d3d9\nf-d3d9-idirect3ddevice9-setviewport.md) | Sets the viewport parameters for the device. |
| [IDirect3DDevice9::SetViewport](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-setviewport.md) | Sets the viewport parameters for the device. |
| [IDirect3DDevice9::ShowCursor](..\d3d9\nf-d3d9-idirect3ddevice9-showcursor.md) | Displays or hides the cursor. |
| [IDirect3DDevice9::ShowCursor](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-showcursor.md) | Displays or hides the cursor. |
| [IDirect3DDevice9::StretchRect](..\d3d9\nf-d3d9-idirect3ddevice9-stretchrect.md) | Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream. |
| [IDirect3DDevice9::StretchRect](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-stretchrect.md) | Copy the contents of the source rectangle to the destination rectangle. The source rectangle can be stretched and filtered by the copy. This function is often used to change the aspect ratio of a video stream. |
| [IDirect3DDevice9::TestCooperativeLevel](..\d3d9\nf-d3d9-idirect3ddevice9-testcooperativelevel.md) | Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application. |
| [IDirect3DDevice9::TestCooperativeLevel](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-testcooperativelevel.md) | Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application. |
| [IDirect3DDevice9::UpdateSurface](..\d3d9\nf-d3d9-idirect3ddevice9-updatesurface.md) | Copies rectangular subsets of pixels from one surface to another. |
| [IDirect3DDevice9::UpdateSurface](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-updatesurface.md) | Copies rectangular subsets of pixels from one surface to another. |
| [IDirect3DDevice9::UpdateTexture](..\d3d9\nf-d3d9-idirect3ddevice9-updatetexture.md) | Updates the dirty portions of a texture. |
| [IDirect3DDevice9::UpdateTexture](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-updatetexture.md) | Updates the dirty portions of a texture. |
| [IDirect3DDevice9::ValidateDevice](..\d3d9\nf-d3d9-idirect3ddevice9-validatedevice.md) | Reports the device's ability to render the current texture-blending operations and arguments in a single pass. |
| [IDirect3DDevice9::ValidateDevice](..\d3d9helper\nf-d3d9helper-idirect3ddevice9-validatedevice.md) | Reports the device's ability to render the current texture-blending operations and arguments in a single pass. |
| [IDirect3DDevice9Ex::CheckDeviceState](..\d3d9\nf-d3d9-idirect3ddevice9ex-checkdevicestate.md) | Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application. |
| [IDirect3DDevice9Ex::CheckResourceResidency](..\d3d9\nf-d3d9-idirect3ddevice9ex-checkresourceresidency.md) | Checks an array of resources to determine if it is likely that they will cause a large stall at Draw time because the system must make the resources GPU-accessible. |
| [IDirect3DDevice9Ex::ComposeRects](..\d3d9\nf-d3d9-idirect3ddevice9ex-composerects.md) | Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations. |
| [IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx](..\d3d9\nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex.md) | Creates a depth-stencil surface. |
| [IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx](..\d3d9\nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex.md) | Create an off-screen surface. |
| [IDirect3DDevice9Ex::CreateRenderTargetEx](..\d3d9\nf-d3d9-idirect3ddevice9ex-createrendertargetex.md) | Creates a render-target surface. |
| [IDirect3DDevice9Ex::GetDisplayModeEx](..\d3d9\nf-d3d9-idirect3ddevice9ex-getdisplaymodeex.md) | Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings. |
| [IDirect3DDevice9Ex::GetGPUThreadPriority](..\d3d9\nf-d3d9-idirect3ddevice9ex-getgputhreadpriority.md) | Get the priority of the GPU thread. |
| [IDirect3DDevice9Ex::GetMaximumFrameLatency](..\d3d9\nf-d3d9-idirect3ddevice9ex-getmaximumframelatency.md) | Retrieves the number of frames of data that the system is allowed to queue. |
| [IDirect3DDevice9Ex::PresentEx](..\d3d9\nf-d3d9-idirect3ddevice9ex-presentex.md) | Swap the swapchain's next buffer with the front buffer. |
| [IDirect3DDevice9Ex::ResetEx](..\d3d9\nf-d3d9-idirect3ddevice9ex-resetex.md) | Resets the type, size, and format of the swap chain with all other surfaces persistent. |
| [IDirect3DDevice9Ex::SetConvolutionMonoKernel](..\d3d9\nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel.md) | Prepare the texture sampler for monochrome convolution filtering on a single-color texture. |
| [IDirect3DDevice9Ex::SetGPUThreadPriority](..\d3d9\nf-d3d9-idirect3ddevice9ex-setgputhreadpriority.md) | Set the priority on the GPU thread. |
| [IDirect3DDevice9Ex::SetMaximumFrameLatency](..\d3d9\nf-d3d9-idirect3ddevice9ex-setmaximumframelatency.md) | Set the number of frames that the system is allowed to queue for rendering. |
| [IDirect3DDevice9Ex::TestCooperativeLevel](..\d3d9\nf-d3d9-idirect3ddevice9ex-testcooperativelevel.md) | Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application. |
| [IDirect3DDevice9Ex::WaitForVBlank](..\d3d9\nf-d3d9-idirect3ddevice9ex-waitforvblank.md) | Suspend execution of the calling thread until the next vertical blank signal. |
| [IDirect3DIndexBuffer9::GetDesc](..\d3d9\nf-d3d9-idirect3dindexbuffer9-getdesc.md) | Retrieves a description of the index buffer resource. |
| [IDirect3DIndexBuffer9::GetDesc](..\d3d9helper\nf-d3d9helper-idirect3dindexbuffer9-getdesc.md) | Retrieves a description of the index buffer resource. |
| [IDirect3DIndexBuffer9::Lock](..\d3d9\nf-d3d9-idirect3dindexbuffer9-lock.md) | Locks a range of index data and obtains a pointer to the index buffer memory. |
| [IDirect3DIndexBuffer9::Lock](..\d3d9helper\nf-d3d9helper-idirect3dindexbuffer9-lock.md) | Locks a range of index data and obtains a pointer to the index buffer memory. |
| [IDirect3DIndexBuffer9::Unlock](..\d3d9\nf-d3d9-idirect3dindexbuffer9-unlock.md) | Unlocks index data. |
| [IDirect3DIndexBuffer9::Unlock](..\d3d9helper\nf-d3d9helper-idirect3dindexbuffer9-unlock.md) | Unlocks index data. |
| [IDirect3DPixelShader9::GetDevice](..\d3d9\nf-d3d9-idirect3dpixelshader9-getdevice.md) | Gets the device. |
| [IDirect3DPixelShader9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dpixelshader9-getdevice.md) | Gets the device. |
| [IDirect3DPixelShader9::GetFunction](..\d3d9\nf-d3d9-idirect3dpixelshader9-getfunction.md) | Gets a pointer to the shader data. |
| [IDirect3DPixelShader9::GetFunction](..\d3d9helper\nf-d3d9helper-idirect3dpixelshader9-getfunction.md) | Gets a pointer to the shader data. |
| [IDirect3DQuery9::GetDataSize](..\d3d9\nf-d3d9-idirect3dquery9-getdatasize.md) | Gets the number of bytes in the query data. |
| [IDirect3DQuery9::GetDataSize](..\d3d9helper\nf-d3d9helper-idirect3dquery9-getdatasize.md) | Gets the number of bytes in the query data. |
| [IDirect3DQuery9::GetData](..\d3d9\nf-d3d9-idirect3dquery9-getdata.md) | Polls a queried resource to get the query state or a query result. For more information about queries, see Queries (Direct3D 9). |
| [IDirect3DQuery9::GetData](..\d3d9helper\nf-d3d9helper-idirect3dquery9-getdata.md) | Polls a queried resource to get the query state or a query result. For more information about queries, see Queries (Direct3D 9). |
| [IDirect3DQuery9::GetDevice](..\d3d9\nf-d3d9-idirect3dquery9-getdevice.md) | Gets the device that is being queried. |
| [IDirect3DQuery9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dquery9-getdevice.md) | Gets the device that is being queried. |
| [IDirect3DQuery9::GetType](..\d3d9\nf-d3d9-idirect3dquery9-gettype.md) | Gets the query type. |
| [IDirect3DQuery9::GetType](..\d3d9helper\nf-d3d9helper-idirect3dquery9-gettype.md) | Gets the query type. |
| [IDirect3DQuery9::Issue](..\d3d9\nf-d3d9-idirect3dquery9-issue.md) | Issue a query. |
| [IDirect3DQuery9::Issue](..\d3d9helper\nf-d3d9helper-idirect3dquery9-issue.md) | Issue a query. |
| [IDirect3DResource9::FreePrivateData](..\d3d9\nf-d3d9-idirect3dresource9-freeprivatedata.md) | Frees the specified private data associated with this resource. |
| [IDirect3DResource9::FreePrivateData](..\d3d9helper\nf-d3d9helper-idirect3dresource9-freeprivatedata.md) | Frees the specified private data associated with this resource. |
| [IDirect3DResource9::GetDevice](..\d3d9\nf-d3d9-idirect3dresource9-getdevice.md) | Retrieves the device associated with a resource. |
| [IDirect3DResource9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dresource9-getdevice.md) | Retrieves the device associated with a resource. |
| [IDirect3DResource9::GetPriority](..\d3d9\nf-d3d9-idirect3dresource9-getpriority.md) | Retrieves the priority for this resource. |
| [IDirect3DResource9::GetPriority](..\d3d9helper\nf-d3d9helper-idirect3dresource9-getpriority.md) | Retrieves the priority for this resource. |
| [IDirect3DResource9::GetPrivateData](..\d3d9\nf-d3d9-idirect3dresource9-getprivatedata.md) | Copies the private data associated with the resource to a provided buffer. |
| [IDirect3DResource9::GetPrivateData](..\d3d9helper\nf-d3d9helper-idirect3dresource9-getprivatedata.md) | Copies the private data associated with the resource to a provided buffer. |
| [IDirect3DResource9::GetType](..\d3d9\nf-d3d9-idirect3dresource9-gettype.md) | Returns the type of the resource. |
| [IDirect3DResource9::GetType](..\d3d9helper\nf-d3d9helper-idirect3dresource9-gettype.md) | Returns the type of the resource. |
| [IDirect3DResource9::PreLoad](..\d3d9\nf-d3d9-idirect3dresource9-preload.md) | Preloads a managed resource. |
| [IDirect3DResource9::PreLoad](..\d3d9helper\nf-d3d9helper-idirect3dresource9-preload.md) | Preloads a managed resource. |
| [IDirect3DResource9::SetPriority](..\d3d9\nf-d3d9-idirect3dresource9-setpriority.md) | Assigns the priority of a resource for scheduling purposes. |
| [IDirect3DResource9::SetPriority](..\d3d9helper\nf-d3d9helper-idirect3dresource9-setpriority.md) | Assigns the priority of a resource for scheduling purposes. |
| [IDirect3DResource9::SetPrivateData](..\d3d9\nf-d3d9-idirect3dresource9-setprivatedata.md) | Associates data with the resource that is intended for use by the application, not by Direct3D. Data is passed by value, and multiple sets of data can be associated with a single resource. |
| [IDirect3DResource9::SetPrivateData](..\d3d9helper\nf-d3d9helper-idirect3dresource9-setprivatedata.md) | Associates data with the resource that is intended for use by the application, not by Direct3D. Data is passed by value, and multiple sets of data can be associated with a single resource. |
| [IDirect3DStateBlock9::Apply](..\d3d9\nf-d3d9-idirect3dstateblock9-apply.md) | Apply the state block to the current device state. |
| [IDirect3DStateBlock9::Apply](..\d3d9helper\nf-d3d9helper-idirect3dstateblock9-apply.md) | Apply the state block to the current device state. |
| [IDirect3DStateBlock9::Capture](..\d3d9\nf-d3d9-idirect3dstateblock9-capture.md) | Capture the current value of states that are included in a stateblock. |
| [IDirect3DStateBlock9::Capture](..\d3d9helper\nf-d3d9helper-idirect3dstateblock9-capture.md) | Capture the current value of states that are included in a stateblock. |
| [IDirect3DStateBlock9::GetDevice](..\d3d9\nf-d3d9-idirect3dstateblock9-getdevice.md) | Gets the device. |
| [IDirect3DStateBlock9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dstateblock9-getdevice.md) | Gets the device. |
| [IDirect3DSurface9::GetContainer](..\d3d9\nf-d3d9-idirect3dsurface9-getcontainer.md) | Provides access to the parent cube texture or texture (mipmap) object, if this surface is a child level of a cube texture or a mipmap. This method can also provide access to the parent swap chain if the surface is a back-buffer child. |
| [IDirect3DSurface9::GetContainer](..\d3d9helper\nf-d3d9helper-idirect3dsurface9-getcontainer.md) | Provides access to the parent cube texture or texture (mipmap) object, if this surface is a child level of a cube texture or a mipmap. This method can also provide access to the parent swap chain if the surface is a back-buffer child. |
| [IDirect3DSurface9::GetDC](..\d3d9\nf-d3d9-idirect3dsurface9-getdc.md) | Retrieves a device context. |
| [IDirect3DSurface9::GetDC](..\d3d9helper\nf-d3d9helper-idirect3dsurface9-getdc.md) | Retrieves a device context. |
| [IDirect3DSurface9::GetDesc](..\d3d9\nf-d3d9-idirect3dsurface9-getdesc.md) | Retrieves a description of the surface. |
| [IDirect3DSurface9::GetDesc](..\d3d9helper\nf-d3d9helper-idirect3dsurface9-getdesc.md) | Retrieves a description of the surface. |
| [IDirect3DSurface9::LockRect](..\d3d9\nf-d3d9-idirect3dsurface9-lockrect.md) | Locks a rectangle on a surface. |
| [IDirect3DSurface9::LockRect](..\d3d9helper\nf-d3d9helper-idirect3dsurface9-lockrect.md) | Locks a rectangle on a surface. |
| [IDirect3DSurface9::ReleaseDC](..\d3d9\nf-d3d9-idirect3dsurface9-releasedc.md) | Release a device context handle. |
| [IDirect3DSurface9::ReleaseDC](..\d3d9helper\nf-d3d9helper-idirect3dsurface9-releasedc.md) | Release a device context handle. |
| [IDirect3DSurface9::UnlockRect](..\d3d9\nf-d3d9-idirect3dsurface9-unlockrect.md) | Unlocks a rectangle on a surface. |
| [IDirect3DSurface9::UnlockRect](..\d3d9helper\nf-d3d9helper-idirect3dsurface9-unlockrect.md) | Unlocks a rectangle on a surface. |
| [IDirect3DSwapChain9::GetBackBuffer](..\d3d9\nf-d3d9-idirect3dswapchain9-getbackbuffer.md) | Retrieves a back buffer from the swap chain of the device. |
| [IDirect3DSwapChain9::GetBackBuffer](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-getbackbuffer.md) | Retrieves a back buffer from the swap chain of the device. |
| [IDirect3DSwapChain9::GetDevice](..\d3d9\nf-d3d9-idirect3dswapchain9-getdevice.md) | Retrieves the device associated with the swap chain. |
| [IDirect3DSwapChain9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-getdevice.md) | Retrieves the device associated with the swap chain. |
| [IDirect3DSwapChain9::GetDisplayMode](..\d3d9\nf-d3d9-idirect3dswapchain9-getdisplaymode.md) | Retrieves the display mode's spatial resolution, color resolution, and refresh frequency. |
| [IDirect3DSwapChain9::GetDisplayMode](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-getdisplaymode.md) | Retrieves the display mode's spatial resolution, color resolution, and refresh frequency. |
| [IDirect3DSwapChain9::GetFrontBufferData](..\d3d9\nf-d3d9-idirect3dswapchain9-getfrontbufferdata.md) | Generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application. |
| [IDirect3DSwapChain9::GetFrontBufferData](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-getfrontbufferdata.md) | Generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application. |
| [IDirect3DSwapChain9::GetPresentParameters](..\d3d9\nf-d3d9-idirect3dswapchain9-getpresentparameters.md) | Retrieves the presentation parameters associated with a swap chain. |
| [IDirect3DSwapChain9::GetPresentParameters](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-getpresentparameters.md) | Retrieves the presentation parameters associated with a swap chain. |
| [IDirect3DSwapChain9::GetRasterStatus](..\d3d9\nf-d3d9-idirect3dswapchain9-getrasterstatus.md) | Returns information describing the raster of the monitor on which the swap chain is presented. |
| [IDirect3DSwapChain9::GetRasterStatus](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-getrasterstatus.md) | Returns information describing the raster of the monitor on which the swap chain is presented. |
| [IDirect3DSwapChain9::Present](..\d3d9\nf-d3d9-idirect3dswapchain9-present.md) | Presents the contents of the next buffer in the sequence of back buffers owned by the swap chain. |
| [IDirect3DSwapChain9::Present](..\d3d9helper\nf-d3d9helper-idirect3dswapchain9-present.md) | Presents the contents of the next buffer in the sequence of back buffers owned by the swap chain. |
| [IDirect3DSwapChain9Ex::GetDisplayModeEx](..\d3d9\nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex.md) | Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings. |
| [IDirect3DSwapChain9Ex::GetLastPresentCount](..\d3d9\nf-d3d9-idirect3dswapchain9ex-getlastpresentcount.md) | Returns the number of times the swapchain has been processed. |
| [IDirect3DTexture9::AddDirtyRect](..\d3d9\nf-d3d9-idirect3dtexture9-adddirtyrect.md) | Adds a dirty region to a texture resource. |
| [IDirect3DTexture9::AddDirtyRect](..\d3d9helper\nf-d3d9helper-idirect3dtexture9-adddirtyrect.md) | Adds a dirty region to a texture resource. |
| [IDirect3DTexture9::GetLevelDesc](..\d3d9\nf-d3d9-idirect3dtexture9-getleveldesc.md) | Retrieves a level description of a texture resource. |
| [IDirect3DTexture9::GetLevelDesc](..\d3d9helper\nf-d3d9helper-idirect3dtexture9-getleveldesc.md) | Retrieves a level description of a texture resource. |
| [IDirect3DTexture9::GetSurfaceLevel](..\d3d9\nf-d3d9-idirect3dtexture9-getsurfacelevel.md) | Retrieves the specified texture surface level. |
| [IDirect3DTexture9::GetSurfaceLevel](..\d3d9helper\nf-d3d9helper-idirect3dtexture9-getsurfacelevel.md) | Retrieves the specified texture surface level. |
| [IDirect3DTexture9::LockRect](..\d3d9\nf-d3d9-idirect3dtexture9-lockrect.md) | Locks a rectangle on a texture resource. |
| [IDirect3DTexture9::LockRect](..\d3d9helper\nf-d3d9helper-idirect3dtexture9-lockrect.md) | Locks a rectangle on a texture resource. |
| [IDirect3DTexture9::UnlockRect](..\d3d9\nf-d3d9-idirect3dtexture9-unlockrect.md) | Unlocks a rectangle on a texture resource. |
| [IDirect3DTexture9::UnlockRect](..\d3d9helper\nf-d3d9helper-idirect3dtexture9-unlockrect.md) | Unlocks a rectangle on a texture resource. |
| [IDirect3DVertexBuffer9::GetDesc](..\d3d9\nf-d3d9-idirect3dvertexbuffer9-getdesc.md) | Retrieves a description of the vertex buffer resource. |
| [IDirect3DVertexBuffer9::GetDesc](..\d3d9helper\nf-d3d9helper-idirect3dvertexbuffer9-getdesc.md) | Retrieves a description of the vertex buffer resource. |
| [IDirect3DVertexBuffer9::Lock](..\d3d9\nf-d3d9-idirect3dvertexbuffer9-lock.md) | Locks a range of vertex data and obtains a pointer to the vertex buffer memory. |
| [IDirect3DVertexBuffer9::Lock](..\d3d9helper\nf-d3d9helper-idirect3dvertexbuffer9-lock.md) | Locks a range of vertex data and obtains a pointer to the vertex buffer memory. |
| [IDirect3DVertexBuffer9::Unlock](..\d3d9\nf-d3d9-idirect3dvertexbuffer9-unlock.md) | Unlocks vertex data. |
| [IDirect3DVertexBuffer9::Unlock](..\d3d9helper\nf-d3d9helper-idirect3dvertexbuffer9-unlock.md) | Unlocks vertex data. |
| [IDirect3DVertexDeclaration9::GetDeclaration](..\d3d9\nf-d3d9-idirect3dvertexdeclaration9-getdeclaration.md) | Gets the vertex shader declaration. |
| [IDirect3DVertexDeclaration9::GetDeclaration](..\d3d9helper\nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration.md) | Gets the vertex shader declaration. |
| [IDirect3DVertexDeclaration9::GetDevice](..\d3d9\nf-d3d9-idirect3dvertexdeclaration9-getdevice.md) | Gets the current device. |
| [IDirect3DVertexDeclaration9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dvertexdeclaration9-getdevice.md) | Gets the current device. |
| [IDirect3DVertexShader9::GetDevice](..\d3d9\nf-d3d9-idirect3dvertexshader9-getdevice.md) | Gets the device. |
| [IDirect3DVertexShader9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dvertexshader9-getdevice.md) | Gets the device. |
| [IDirect3DVertexShader9::GetFunction](..\d3d9\nf-d3d9-idirect3dvertexshader9-getfunction.md) | Gets a pointer to the shader data. |
| [IDirect3DVertexShader9::GetFunction](..\d3d9helper\nf-d3d9helper-idirect3dvertexshader9-getfunction.md) | Gets a pointer to the shader data. |
| [IDirect3DVolume9::FreePrivateData](..\d3d9\nf-d3d9-idirect3dvolume9-freeprivatedata.md) | Frees the specified private data associated with this volume. |
| [IDirect3DVolume9::FreePrivateData](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-freeprivatedata.md) | Frees the specified private data associated with this volume. |
| [IDirect3DVolume9::GetContainer](..\d3d9\nf-d3d9-idirect3dvolume9-getcontainer.md) | Provides access to the parent volume texture object, if this surface is a child level of a volume texture. |
| [IDirect3DVolume9::GetContainer](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-getcontainer.md) | Provides access to the parent volume texture object, if this surface is a child level of a volume texture. |
| [IDirect3DVolume9::GetDesc](..\d3d9\nf-d3d9-idirect3dvolume9-getdesc.md) | Retrieves a description of the volume. |
| [IDirect3DVolume9::GetDesc](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-getdesc.md) | Retrieves a description of the volume. |
| [IDirect3DVolume9::GetDevice](..\d3d9\nf-d3d9-idirect3dvolume9-getdevice.md) | Retrieves the device associated with a volume. |
| [IDirect3DVolume9::GetDevice](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-getdevice.md) | Retrieves the device associated with a volume. |
| [IDirect3DVolume9::GetPrivateData](..\d3d9\nf-d3d9-idirect3dvolume9-getprivatedata.md) | Copies the private data associated with the volume to a provided buffer. |
| [IDirect3DVolume9::GetPrivateData](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-getprivatedata.md) | Copies the private data associated with the volume to a provided buffer. |
| [IDirect3DVolume9::LockBox](..\d3d9\nf-d3d9-idirect3dvolume9-lockbox.md) | Locks a box on a volume resource. |
| [IDirect3DVolume9::LockBox](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-lockbox.md) | Locks a box on a volume resource. |
| [IDirect3DVolume9::SetPrivateData](..\d3d9\nf-d3d9-idirect3dvolume9-setprivatedata.md) | Associates data with the volume that is intended for use by the application, not by Direct3D. |
| [IDirect3DVolume9::SetPrivateData](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-setprivatedata.md) | Associates data with the volume that is intended for use by the application, not by Direct3D. |
| [IDirect3DVolume9::UnlockBox](..\d3d9\nf-d3d9-idirect3dvolume9-unlockbox.md) | Unlocks a box on a volume resource. |
| [IDirect3DVolume9::UnlockBox](..\d3d9helper\nf-d3d9helper-idirect3dvolume9-unlockbox.md) | Unlocks a box on a volume resource. |
| [IDirect3DVolumeTexture9::AddDirtyBox](..\d3d9\nf-d3d9-idirect3dvolumetexture9-adddirtybox.md) | Adds a dirty region to a volume texture resource. |
| [IDirect3DVolumeTexture9::AddDirtyBox](..\d3d9helper\nf-d3d9helper-idirect3dvolumetexture9-adddirtybox.md) | Adds a dirty region to a volume texture resource. |
| [IDirect3DVolumeTexture9::GetLevelDesc](..\d3d9\nf-d3d9-idirect3dvolumetexture9-getleveldesc.md) | Retrieves a level description of a volume texture resource. |
| [IDirect3DVolumeTexture9::GetLevelDesc](..\d3d9helper\nf-d3d9helper-idirect3dvolumetexture9-getleveldesc.md) | Retrieves a level description of a volume texture resource. |
| [IDirect3DVolumeTexture9::GetVolumeLevel](..\d3d9\nf-d3d9-idirect3dvolumetexture9-getvolumelevel.md) | Retrieves the specified volume texture level. |
| [IDirect3DVolumeTexture9::GetVolumeLevel](..\d3d9helper\nf-d3d9helper-idirect3dvolumetexture9-getvolumelevel.md) | Retrieves the specified volume texture level. |
| [IDirect3DVolumeTexture9::LockBox](..\d3d9\nf-d3d9-idirect3dvolumetexture9-lockbox.md) | Locks a box on a volume texture resource. |
| [IDirect3DVolumeTexture9::LockBox](..\d3d9helper\nf-d3d9helper-idirect3dvolumetexture9-lockbox.md) | Locks a box on a volume texture resource. |
| [IDirect3DVolumeTexture9::UnlockBox](..\d3d9\nf-d3d9-idirect3dvolumetexture9-unlockbox.md) | Unlocks a box on a volume texture resource. |
| [IDirect3DVolumeTexture9::UnlockBox](..\d3d9helper\nf-d3d9helper-idirect3dvolumetexture9-unlockbox.md) | Unlocks a box on a volume texture resource. |
