---
UID: NF:olectl.OleLoadPictureFile
title: OleLoadPictureFile function (olectl.h)
description: Creates an IPictureDisp object from a picture file on disk.
helpviewer_keywords: ["OleLoadPictureFile","OleLoadPictureFile function [Automation]","_oa96_OleLoadPictureFile","automat.oleloadpicturefile","olectl/OleLoadPictureFile"]
old-location: automat\oleloadpicturefile.htm
tech.root: automat
ms.assetid: ecfbf297-88fa-42bf-afa7-f7884be17b15
ms.date: 12/05/2018
ms.keywords: OleLoadPictureFile, OleLoadPictureFile function [Automation], _oa96_OleLoadPictureFile, automat.oleloadpicturefile, olectl/OleLoadPictureFile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleLoadPictureFile
 - olectl/OleLoadPictureFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleLoadPictureFile
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

