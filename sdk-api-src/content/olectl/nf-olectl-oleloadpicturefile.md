---
UID: NF:olectl.OleLoadPictureFile
title: OleLoadPictureFile function
author: windows-sdk-content
description: Creates an IPictureDisp object from a picture file on disk.
old-location: automat\oleloadpicturefile.htm
tech.root: automat
ms.assetid: ecfbf297-88fa-42bf-afa7-f7884be17b15
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OleLoadPictureFile, OleLoadPictureFile function [Automation], _oa96_OleLoadPictureFile, automat.oleloadpicturefile, olectl/OleLoadPictureFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: olectl.h
req.include-header: 
req.target-type: Windows
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleLoadPictureFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleLoadPictureFile function


## -description


Creates an <b>IPictureDisp</b> object from a picture file on disk.


## -parameters




### -param varFileName [in]

The path and name of the picture file to load.


### -param lplpdispPicture [out]

The location that receives a pointer to the <b>IPictureDisp</b> object.


## -returns



This method returns standard COM error codes in addition to the following values.



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
The method completed successfully.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CTL_E_INVALIDPICTURE</b></dt>
</dl>
</td>
<td width="60%">
Invalid picture file.

</td>
</tr>
</table>
 




## -remarks



Recognized graphic formats include bitmap (.bmp), JPEG (.jpg), GIF (.gif), and PGN (.png) files.



