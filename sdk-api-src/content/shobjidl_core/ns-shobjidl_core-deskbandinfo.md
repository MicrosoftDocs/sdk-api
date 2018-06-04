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

# DESKBANDINFO structure


## -description


Receives information about a band object. This structure is used with the deprecated <a href="https://msdn.microsoft.com/7567a2f8-989e-4d11-ae55-209e4cfacad0">IDeskBand::GetBandInfo</a> method.


## -struct-fields




### -field dwMask

Type: <b>DWORD</b>

The set of flags that determine which members of this structure are being requested by the caller. One or more of the following values:



#### DBIM_MINSIZE

<b>ptMinSize</b> is requested.



#### DBIM_MAXSIZE

<b>ptMaxSize</b> is requested.



#### DBIM_INTEGRAL

<b>ptIntegral</b> is requested.



#### DBIM_ACTUAL

<b>ptActual</b> is requested.



#### DBIM_TITLE

<b>wszTitle</b> is requested.



#### DBIM_MODEFLAGS

<b>dwModeFlags</b> is requested.



#### DBIM_BKCOLOR

<b>crBkgnd</b> is requested.


### -field ptMinSize

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that receives the minimum size of the band object. The minimum width is given in the <b>POINTL</b> structure's <b>x</b> member and the minimum height is given in the <b>y</b> member.


### -field ptMaxSize

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that receives the maximum size of the band object. The maximum height is given in the <b>POINTL</b> structure's <b>y</b> member and the <b>x</b> member is ignored. If the band object has no limit for its maximum height, (LONG)-1 should be used.


### -field ptIntegral

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that receives the sizing step value (increment) in which the band object is resized. The vertical step value is given in the <b>POINTL</b> structure's <b>y</b> member and the <b>x</b> member is ignored.

The <b>dwModeFlags</b> member must contain the DBIMF_VARIABLEHEIGHT flag; otherwise, <b>ptIntegral</b> is ignored.


### -field ptActual

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that receives the ideal size of the band object. The ideal width is given in the <b>POINTL</b> structure's <b>x</b> member and the ideal height is given in the <b>y</b> member. The band container attempts to use these values, but the band is not guaranteed to be this size.


### -field wszTitle

Type: <b>WCHAR[256]</b>

A <b>WCHAR</b> buffer that receives the title of the band.


### -field dwModeFlags

Type: <b>DWORD</b>

A value that receives a set of flags that specify the mode of operation for the band object. One or more of the following values:



#### DBIMF_NORMAL

The band uses default properties. The other mode flags modify this flag.



#### DBIMF_FIXED

<b>Windows XP and later:</b> The band object is of a fixed sized and position. With this flag, a sizing grip is not displayed on the band object.



#### DBIMF_FIXEDBMP

<b>Windows XP and later:</b> The band object uses a fixed bitmap (.bmp) file as its background. Note that backgrounds are not supported in all cases, so the bitmap may not be seen even when this flag is set.



#### DBIMF_VARIABLEHEIGHT

The height of the band object can be changed. The <b>ptIntegral</b> member defines the step value by which the band object can be resized.



#### DBIMF_UNDELETEABLE

<b>Windows XP and later:</b> The band object cannot be removed from the band container.



#### DBIMF_DEBOSSED

The band object is displayed with a sunken appearance.



#### DBIMF_BKCOLOR

The band is displayed with the background color specified in <b>crBkgnd</b>.



#### DBIMF_USECHEVRON

<b>Windows XP and later:</b> If the full band object cannot be displayed (that is, the band object is smaller than <b>ptActual</b>, a chevron is shown to indicate that there are more options available. These options are displayed when the chevron is clicked.



#### DBIMF_BREAK

<b>Windows XP and later:</b> The band object is displayed in a new row in the band container.



#### DBIMF_ADDTOFRONT

<b>Windows XP and later:</b> The band object is the first object in the band container.



#### DBIMF_TOPALIGN

<b>Windows XP and later:</b> The band object is displayed in the top row of the band container.



#### DBIMF_NOGRIPPER

<b>Windows Vista and later:</b> No sizing grip is ever displayed to allow the user to move or resize the band object.



#### DBIMF_ALWAYSGRIPPER

<b>Windows Vista and later:</b> A sizing grip that allows the user to move or resize the band object is always shown, even if that band object is the only one in the container.



#### DBIMF_NOMARGINS

<b>Windows Vista and later:</b> The band object should not display margins.


### -field crBkgnd

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure that receives the background color of the band. The <b>dwModeFlags</b> member must contain the <b>DBIMF_BKCOLOR</b> flag; otherwise, <b>crBkgnd</b> is ignored.

