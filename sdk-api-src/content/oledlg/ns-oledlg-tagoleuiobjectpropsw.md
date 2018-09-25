---
UID: NS:oledlg.tagOLEUIOBJECTPROPSW
title: tagOLEUIOBJECTPROPSW
author: windows-sdk-content
description: Contains information that is used to initialize the standard Object Properties dialog box.
old-location: com\oleuiobjectprops_struct.htm
tech.root: com
ms.assetid: 7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPOLEUIOBJECTPROPSW, *POLEUIOBJECTPROPSW, LPOLEUIOBJECTPROPS, LPOLEUIOBJECTPROPS structure pointer [COM], OLEUIOBJECTPROPS, OLEUIOBJECTPROPS structure [COM], OLEUIOBJECTPROPSA, OLEUIOBJECTPROPSW, OPF_DISABLECONVERT, OPF_NOFILLDEFAULT, OPF_OBJECTISLINK, OPF_SHOWHELP, POLEUIOBJECTPROPS, POLEUIOBJECTPROPS structure pointer [COM], _ole_OLEUIOBJECTPROPS, com.oleuiobjectprops_struct, oledlg/LPOLEUIOBJECTPROPS, oledlg/OLEUIOBJECTPROPS, oledlg/OLEUIOBJECTPROPSA, oledlg/OLEUIOBJECTPROPSW, oledlg/POLEUIOBJECTPROPS, tagOLEUIOBJECTPROPSW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIOBJECTPROPSW (Unicode) and OLEUIOBJECTPROPSA (ANSI)
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
 - OleDlg.h
api_name:
 - OLEUIOBJECTPROPS
 - OLEUIOBJECTPROPSA
 - OLEUIOBJECTPROPSW
product: Windows
targetos: Windows
req.typenames: OLEUIOBJECTPROPSW, *POLEUIOBJECTPROPSW, *LPOLEUIOBJECTPROPSW
req.redist: 
---

# tagOLEUIOBJECTPROPSW structure


## -description


Contains information that is used to initialize the standard <b>Object Properties</b> dialog box. It contains references to interfaces used to gather information about the embedding or link, references to three structures that are used to initialize the default tabs â€” <b>General</b> (<a href="https://msdn.microsoft.com/851d66c8-94a7-47ab-95f4-12a34897de20">OLEUIGNRLPROPS</a>), <b>View</b> (<a href="https://msdn.microsoft.com/e45565c5-185e-4143-a5c2-d0b273b5086e">OLEUIVIEWPROPS</a>), and <b>Link</b> (<a href="https://msdn.microsoft.com/3f355ce8-adc3-4878-a8b4-3f7d94547ef1">OLEUILINKPROPS</a>), if appropriate â€” and a standard property-sheet extensibility interface that allows the caller to add additional custom property sheets to the dialog box.




## -struct-fields




### -field cbStruct

The size of the structure, in bytes.


### -field dwFlags

Contains in/out global flags for the property sheet.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPF_OBJECTISLINK"></a><a id="opf_objectislink"></a><dl>
<dt><b>OPF_OBJECTISLINK</b></dt>
</dl>
</td>
<td width="60%">
Object is a link object and therefore has a link property page.

</td>
</tr>
<tr>
<td width="40%"><a id="OPF_NOFILLDEFAULT"></a><a id="opf_nofilldefault"></a><dl>
<dt><b>OPF_NOFILLDEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Do not fill in default values for the object.

</td>
</tr>
<tr>
<td width="40%"><a id="OPF_SHOWHELP"></a><a id="opf_showhelp"></a><dl>
<dt><b>OPF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
The dialog box will display a <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="OPF_DISABLECONVERT"></a><a id="opf_disableconvert"></a><dl>
<dt><b>OPF_DISABLECONVERT</b></dt>
</dl>
</td>
<td width="60%">
The <b>Convert</b> button will be disabled on the general property page.

</td>
</tr>
</table>
 


### -field lpPS

Pointer to the standard property sheet header (<a href="_win32_PROPSHEETHEADER_cpp">PROPSHEETHEADER</a>), used for extensibility.


### -field dwObject

Identifier for the object.


### -field lpObjInfo

Pointer to the interface to manipulate object.


### -field dwLink

Container-defined unique identifier for a single link. Containers can use the pointer to the link's container site for this value.


### -field lpLinkInfo

 Pointer to the interface to manipulate link.


### -field lpGP

 Pointer to the general page data.


### -field lpVP

Pointer to the view page data.


### -field lpLP

Pointer to the link page data.


## -see-also




<a href="https://msdn.microsoft.com/851d66c8-94a7-47ab-95f4-12a34897de20">OLEUIGNRLPROPS</a>



<a href="https://msdn.microsoft.com/3f355ce8-adc3-4878-a8b4-3f7d94547ef1">OLEUILINKPROPS</a>



<a href="https://msdn.microsoft.com/e45565c5-185e-4143-a5c2-d0b273b5086e">OLEUIVIEWPROPS</a>



<a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a>
 

 

