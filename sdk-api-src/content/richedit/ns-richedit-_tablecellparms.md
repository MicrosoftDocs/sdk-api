---
UID: NS:richedit._tableCellParms
title: "_tableCellParms"
author: windows-sdk-content
description: Defines the attributes of cells in a table row.
old-location: controls\tablecellparms.htm
old-project: Controls
ms.assetid: 75bf07bd-103b-4f35-b421-5a7559c7b90e
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: TABLECELLPARMS, TABLECELLPARMS structure [Windows Controls], _tableCellParms, controls.tablecellparms, richedit/TABLECELLPARMS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TABLECELLPARMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - TABLECELLPARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _tableCellParms structure


## -description


Defines the attributes of cells in a table row. The definitions include the corresponding Rich Text Format (RTF) control words, which are defined in the <a href="http://go.microsoft.com/fwlink/p/?linkid=239794">Rich Text Format (RTF) Specification</a>. 



## -struct-fields




### -field dxWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The width of a cell (\cellx). 


### -field nVertAlign

 


### -field fMergeTop

 


### -field fMergePrev

 


### -field fVertical

 


### -field fMergeStart

 


### -field fMergeCont

 


### -field wShading

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Shading in .01% (\clshdng). This controls the amount of pattern foreground color (<b>crForePat</b>) and pattern background color (<b>crBackPat</b>) that is used to create the cell background color. If <b>wShading</b> is 0, the cell background is <b>crBackPat</b>. If it’s 10000, the cell background is <b>crForePat</b>. Values of <b>wShading</b> in between are mixtures of the two pattern colors. 



### -field dxBrdrLeft

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Left border width, in twips  (\clbrdrl\brdrwN).


### -field dyBrdrTop

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Top border width (\clbrdrt\brdrwN).


### -field dxBrdrRight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Right border width (\clbrdrr\brdrwN).


### -field dyBrdrBottom

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Bottom border width (\clbrdrb\brdrwN).


### -field crBrdrLeft

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Left border color (\clbrdrl\brdrcf).


### -field crBrdrTop

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Top border color (\clbrdrt\brdrcf).


### -field crBrdrRight

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Right border color (\clbrdrr\brdrcf).


### -field crBrdrBottom

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Bottom border color (\clbrdrb\brdrcf).


### -field crBackPat

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Background color (\clcbpat).


### -field crForePat

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Foreground color (\clcfpat).


#### - fMergeCont:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Merge with the previous cell (\clmrg).


#### - fMergePrev:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Merge with the cell above (\clvmrg).


#### - fMergeStart:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Start set of horizontally merged cells (\clmgf).


#### - fMergeTop:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Top cell for vertical merge (\clvmgf).


#### - fVertical:1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Display text top to bottom, right to left (\cltxtbrlv).


#### - nVertAlign:2

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>


The vertical alignment of cells (\clvertalt (def), \clvertalc, \clvertalb). It can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The content appears at the top of a cell. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The content is centered in the cell.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The content appears at the bottom of a cell. 

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/7F9B2F28-1035-44AA-9DF6-57BC62886A4E">EM_INSERTTABLE</a>



<a href="https://msdn.microsoft.com/8b538d72-1210-4344-b673-592ef9a8cc85">TABLEROWPARMS</a>
 

 

