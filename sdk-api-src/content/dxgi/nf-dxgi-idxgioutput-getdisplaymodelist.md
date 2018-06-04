---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDXGIOutput::GetDisplayModeList


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDisplayModeList</b> anymore to retrieve the matching display mode. Instead, use <a href="https://msdn.microsoft.com/49522ED9-30AD-4F39-96D2-BB6677D72349">IDXGIOutput1::GetDisplayModeList1</a>, which supports stereo display mode.]

Gets the display modes that match the requested format and other input options.


## -parameters




### -param EnumFormat

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The color format (see <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>).


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Options for modes to include (see <a href="https://msdn.microsoft.com/7e0f5629-f8e2-478b-b8eb-00780a3dcf1f">DXGI_ENUM_MODES</a>).
            DXGI_ENUM_MODES_SCALING needs to be specified to expose the display modes that require scaling.  Centered modes, requiring no 
            scaling and corresponding directly to the display output, are enumerated by default.


### -param pNumModes [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Set <i>pDesc</i> to <b>NULL</b> so that <i>pNumModes</i> returns the number of display modes that match the format and the options.
        Otherwise, <i>pNumModes</i> returns the number of display modes returned in <i>pDesc</i>.


### -param pDesc [out, optional]

Type: <b><a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a>*</b>

A pointer to a list of display modes (see <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a>); set to <b>NULL</b> to get the number of display modes.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>. It is rare, but possible, that the display modes available can change immediately after calling 
      this method, in which case DXGI_ERROR_MORE_DATA is returned (if there is not enough room for all the display modes).  
      If <b>GetDisplayModeList</b> is called from a Remote Desktop Services session (formerly Terminal Services session), DXGI_ERROR_NOT_CURRENTLY_AVAILABLE is returned.




## -remarks



In general, when switching from windowed to full-screen mode, a swap chain automatically chooses a display mode that meets (or exceeds) the resolution, color 
      depth and refresh rate of the swap chain. To exercise more control over the display mode, use this API to poll the set of display modes that are validated 
      against monitor capabilities, or all modes that match the desktop (if the desktop settings are not validated against the monitor).

As shown, this API is designed to be called twice. First to get the number of modes available, and second to return a description of the modes.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
UINT num = 0;
DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;
UINT flags         = DXGI_ENUM_MODES_INTERLACED;

pOutput-&gt;GetDisplayModeList( format, flags, &amp;num, 0);

...

DXGI_MODE_DESC * pDescs = new DXGI_MODE_DESC[num];
pOutput-&gt;GetDisplayModeList( format, flags, &amp;num, pDescs);
      </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

