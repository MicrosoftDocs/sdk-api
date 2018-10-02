---
UID: NS:richole._reobject
title: "_reobject"
author: windows-sdk-content
description: Contains information about an OLE or image object in a rich edit control.
old-location: controls\REOBJECT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\reobject.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: REOBJECT, REOBJECT structure [Windows Controls], REO_ALIGNTORIGHT, REO_BELOWBASELINE, REO_BLANK, REO_CANROTATE, REO_DONTNEEDPALETTE, REO_DYNAMICSIZE, REO_GETMETAFILE, REO_HILITED, REO_INPLACEACTIVE, REO_INVERTEDSELECT, REO_LINK, REO_LINKAVAILABLE, REO_OPEN, REO_OWNERDRAWSELECT, REO_RESIZABLE, REO_SELECTED, REO_STATIC, REO_USEASBACKGROUND, REO_WRAPTEXTAROUND, _reobject, _win32_REOBJECT_str, _win32_REOBJECT_str_cpp, controls.REOBJECT, controls._win32_REOBJECT_str, richole/REOBJECT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richole.h
api_name:
 - REOBJECT
product: Windows
targetos: Windows
req.typenames: REOBJECT
req.redist: 
---

# _reobject structure


## -description


Contains information about an OLE or image object  in a rich edit control.


## -struct-fields




### -field cbStruct

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Structure size, in bytes. 


### -field cp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character position of the object. 


### -field clsid

Type: <b>CLSID</b>

Class identifier of the object. 


### -field poleobj

Type: <b>LPOLEOBJECT</b>

An instance of the <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface for the object. 


### -field pstg

Type: <b>LPSTORAGE</b>

An instance of the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface. This is the storage object associated with the object. 


### -field polesite

Type: <b>LPOLECLIENTSITE</b>

An instance of the <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> interface. This is the object's client site in the rich edit control. This address must have been obtained from the <a href="https://msdn.microsoft.com/en-us/library/Bb774338(v=VS.85).aspx">GetClientSite</a> method. 


### -field sizel

Type: <b>SIZEL</b>

The size of the object. The unit of measure is 0.01 millimeters, which is a HIMETRIC measurement. For more information, see function <a href="https://msdn.microsoft.com/bc446b86-3dde-4460-bc54-1eaa4ad19941">GetMapMode</a>. A 0, 0 on insertion indicates that an object is free to determine its size until the modify flag is turned off. 


### -field dvaspect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Display aspect used. See <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> for an explanation of possible values. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Object status flag. It can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REO_ALIGNTORIGHT"></a><a id="reo_aligntoright"></a><dl>
<dt><b>REO_ALIGNTORIGHT</b></dt>
</dl>
</td>
<td width="60%">
Align the object with the right side of the view. This value is ignored if  REO_WRAPTEXTAROUND is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_BELOWBASELINE"></a><a id="reo_belowbaseline"></a><dl>
<dt><b>REO_BELOWBASELINE</b></dt>
</dl>
</td>
<td width="60%">
The object sits below the baseline of the surrounding text; the default is to sit on the baseline.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_BLANK"></a><a id="reo_blank"></a><dl>
<dt><b>REO_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The object is new. This value gives the object an opportunity to save nothing and be deleted from the control automatically.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_CANROTATE"></a><a id="reo_canrotate"></a><dl>
<dt><b>REO_CANROTATE</b></dt>
</dl>
</td>
<td width="60%">
The object can display itself in a rotated position.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_DONTNEEDPALETTE"></a><a id="reo_dontneedpalette"></a><dl>
<dt><b>REO_DONTNEEDPALETTE</b></dt>
</dl>
</td>
<td width="60%">
The object is rendered before the creation and realization of a half-tone palette. Applies to 32-bit platforms only.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_DYNAMICSIZE"></a><a id="reo_dynamicsize"></a><dl>
<dt><b>REO_DYNAMICSIZE</b></dt>
</dl>
</td>
<td width="60%">
The object always determines its extents and may change despite the modify flag being turned off.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETMETAFILE"></a><a id="reo_getmetafile"></a><dl>
<dt><b>REO_GETMETAFILE</b></dt>
</dl>
</td>
<td width="60%">
The rich edit control retrieved the metafile from the object to correctly determine the object's extents. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_HILITED"></a><a id="reo_hilited"></a><dl>
<dt><b>REO_HILITED</b></dt>
</dl>
</td>
<td width="60%">
The object is currently highlighted to indicate selection. Occurs when focus is in the control and <b>REO_SELECTED</b> is set. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_INPLACEACTIVE"></a><a id="reo_inplaceactive"></a><dl>
<dt><b>REO_INPLACEACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The object is currently inplace active. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_INVERTEDSELECT"></a><a id="reo_invertedselect"></a><dl>
<dt><b>REO_INVERTEDSELECT</b></dt>
</dl>
</td>
<td width="60%">
The object is to be drawn entirely inverted when selected; the default is to be drawn with a border.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_LINK"></a><a id="reo_link"></a><dl>
<dt><b>REO_LINK</b></dt>
</dl>
</td>
<td width="60%">
The object is a link. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_LINKAVAILABLE"></a><a id="reo_linkavailable"></a><dl>
<dt><b>REO_LINKAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The object is a link and is believed to be available. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_OPEN"></a><a id="reo_open"></a><dl>
<dt><b>REO_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The object is currently open in its server. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_OWNERDRAWSELECT"></a><a id="reo_ownerdrawselect"></a><dl>
<dt><b>REO_OWNERDRAWSELECT</b></dt>
</dl>
</td>
<td width="60%">
 The owner draws the selected object.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_RESIZABLE"></a><a id="reo_resizable"></a><dl>
<dt><b>REO_RESIZABLE</b></dt>
</dl>
</td>
<td width="60%">
The object may be resized.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_SELECTED"></a><a id="reo_selected"></a><dl>
<dt><b>REO_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
The object is currently selected in the rich edit control. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_STATIC"></a><a id="reo_static"></a><dl>
<dt><b>REO_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The object is a static object. This flag can be read but not set.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_USEASBACKGROUND"></a><a id="reo_useasbackground"></a><dl>
<dt><b>REO_USEASBACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
Use the object as the background picture.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_WRAPTEXTAROUND"></a><a id="reo_wraptextaround"></a><dl>
<dt><b>REO_WRAPTEXTAROUND</b></dt>
</dl>
</td>
<td width="60%">
Wrap text around the object.

</td>
</tr>
</table>
 


### -field dwUser

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Reserved for user-defined values. 


## -remarks



An OLE or image object  in a rich edit control occupies one character position in the plain text part of the in-memory backing store and have the value U+FFFC. They differ from "in-line objects" such as math objects. In-line objects occupy at least two character positions because they have an in-line object start delimiter (U+FDD0) and end delimiter  (U+FDEF).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774338(v=VS.85).aspx">GetClientSite</a>



<b>Reference</b>
 

 

