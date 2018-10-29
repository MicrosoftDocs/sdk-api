---
UID: NF:olectl.OleSavePictureFile
title: OleSavePictureFile function
author: windows-sdk-content
description: Saves a picture to a file.
old-location: automat\olesavepicturefile.htm
tech.root: automat
ms.assetid: ac46d390-9e08-4f79-a621-60ea75f4acff
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: OleSavePictureFile, OleSavePictureFile function [Automation], _oa96_OleSavePictureFile, automat.olesavepicturefile, olectl/OleSavePictureFile
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
 - OleSavePictureFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleSavePictureFile function


## -description


Saves a picture to a file.


## -parameters




### -param lpdispPicture [in]

Points to the <b>IPictureDisp</b> picture object.


### -param bstrFileName [in]

The name of the file to save the picture to.


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
<dt><b>CTL_E_INVALIDPROPERTYVALUE</b></dt>
</dl>
</td>
<td width="60%">
<i>lpdispPicture</i> is <b>NULL</b>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CTL_E_FILENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
<i>bstrFileName</i> cannot be found.

</td>
</tr>
</table>
 



