---
UID: NF:docobj.IPrint.Print
title: IPrint::Print (docobj.h)
description: Prints an object on the specified printer, using the specified job requirements.
helpviewer_keywords: ["IPrint interface [COM]","Print method","IPrint.Print","IPrint::Print","PRINTFLAG_DONTACTUALLYPRINT","PRINTFLAG_FORCEPROPERTIES","PRINTFLAG_MAYBOTHERUSER","PRINTFLAG_PRINTTOFILE","PRINTFLAG_PROMPTUSER","PRINTFLAG_RECOMPOSETODEVICE","PRINTFLAG_USERMAYCHANGEPRINTER","Print","Print method [COM]","Print method [COM]","IPrint interface","_ctrl_iprint_print","com.iprint_print","docobj/IPrint::Print"]
old-location: com\iprint_print.htm
tech.root: com
ms.assetid: 30554d89-ad80-4d73-b44a-97ae5079feb8
ms.date: 12/05/2018
ms.keywords: IPrint interface [COM],Print method, IPrint.Print, IPrint::Print, PRINTFLAG_DONTACTUALLYPRINT, PRINTFLAG_FORCEPROPERTIES, PRINTFLAG_MAYBOTHERUSER, PRINTFLAG_PRINTTOFILE, PRINTFLAG_PROMPTUSER, PRINTFLAG_RECOMPOSETODEVICE, PRINTFLAG_USERMAYCHANGEPRINTER, Print, Print method [COM], Print method [COM],IPrint interface, _ctrl_iprint_print, com.iprint_print, docobj/IPrint::Print
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
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
 - IPrint::Print
 - docobj/IPrint::Print
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IPrint.Print
---

# IPrint::Print


## -description

Prints an object on the specified printer, using the specified job requirements.

## -parameters

### -param grfFlags [in]

A bitfield specifying print options from the <b>PRINTFLAG</b> enumeration.



#### PRINTFLAG_MAYBOTHERUSER (1)



#### PRINTFLAG_PROMPTUSER (2)



#### PRINTFLAG_USERMAYCHANGEPRINTER (4)



#### PRINTFLAG_RECOMPOSETODEVICE (8)



#### PRINTFLAG_DONTACTUALLYPRINT (16)



#### PRINTFLAG_FORCEPROPERTIES (32)



#### PRINTFLAG_PRINTTOFILE (64)

### -param pptd [in, out]

A pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure that describes the target print device.

### -param ppPageSet [in, out]

A pointer to a <a href="/windows/desktop/api/docobj/ns-docobj-pageset">PAGESET</a> pointer variable that receives a pointer to the structure that indicates which pages are to be printed.

### -param pstgmOptions [in, out]

A pointer to object-specific printing options in a serialized OLE property set. This parameter can be <b>NULL</b> on input or return.

### -param pcallback [in]

A pointer to the <a href="/windows/desktop/api/docobj/nn-docobj-icontinuecallback">IContinueCallback</a> interface on the view site, which is to be periodically polled at human-response speeds to determine whether printing should be abandoned. This parameter can be <b>NULL</b>.

### -param nFirstPage [in]

The page number of the first page to be printed. This value overrides any value previously passed to <a href="/windows/desktop/api/docobj/nf-docobj-iprint-setinitialpagenum">IPrint::SetInitialPageNum</a>.

### -param pcPagesPrinted [out]

A pointer to a variable that receives the actual number of pages that were successfully printed.

### -param pnLastPage [out]

A pointer to a variable that receives the page number of the last page that was printed.

## -returns

This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
<dt><b>PRINT_E_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The print process was canceled before completion. *<i>pcPagesPrinted</i> indicates the number of pages that were in fact successfully printed before this error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PRINT_E_NOSUCHPAGE</b></dt>
</dl>
</td>
<td width="60%">
A page specified in **<i>ppPageSet</i> or <i>nFirstPage</i> does not exist.

</td>
</tr>
</table>

## -remarks

The printer on which the object is to be printed is indicated by the <a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure pointed to by <i>pptd</i>. The <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure in the target device indicates whole-job printer-specific options, such as number of copies, paper size, and print quality. The <b>DEVMODE</b> structure may also contain orientation information in the <b>dmOrientation</b> member (this is indicated in the <b>dmFields</b> member). If present, then this paper orientation should be used; if absent, then natural orientation as determined by the object content is to be used.

Due to the possibility of user input, the parameters <i>pptd</i> and <i>ppPageSet</i> are both [in,out] structures. In the absence of user interaction (that is, if the PRINTFLAG_PROMPTUSER flag is not set), both the target device and the page set will necessarily be the same for input and output. However, if the user is prompted for print options, then the object returns target device and page-set information appropriate to what the user has actually chosen.

The <i>pstgmOptions</i> parameter is also [in,out]. On exit, the object should write to *<i>pstgmOptions</i> any object-specific information that it would need to reproduce this exact print job. Examples might include whether the user selected "sheet, notes, or both" in a spreadsheet application. The data passed is in the format of a serialized property set. The data is normally useful only when passed back in a subsequent call to the same object. Because a subsequent call may specify different user interaction flags, target device, or other settings, the caller can cause the document to be printed multiple times in the same way in slightly different printing contexts.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>