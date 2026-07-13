---
UID: NS:cryptdlg.tagCERT_VIEWPROPERTIES_STRUCT_A
title: CERT_VIEWPROPERTIES_STRUCT_A (cryptdlg.h)
description: The CERT_VIEWPROPERTIES_STRUCT structure defines information used when the CertViewProperties function is called to display a certificate's properties. (ANSI)
helpviewer_keywords: ["*PCERT_VIEWPROPERTIES_STRUCT_A","CERT_VIEWPROPERTIES_STRUCT","CERT_VIEWPROPERTIES_STRUCT structure [Security]","CERT_VIEWPROPERTIES_STRUCT_A","CM_ADD_CERT_STORES","CM_ENABLEHOOK","CM_ENABLETEMPLATE","CM_HIDE_ADVANCEPAGE","CM_HIDE_DETAILPAGE","CM_HIDE_TRUSTPAGE","CM_NO_EDITTRUST","CM_NO_NAMECHANGE","CM_SHOW_HELP","CM_SHOW_HELPICON","PCERT_VIEWPROPERTIES_STRUCT","PCERT_VIEWPROPERTIES_STRUCT structure pointer [Security]","cryptdlg/CERT_VIEWPROPERTIES_STRUCT","cryptdlg/PCERT_VIEWPROPERTIES_STRUCT","security.cert_viewproperties_struct"]
old-location: security\cert_viewproperties_struct.htm
tech.root: security
ms.assetid: 3d18526b-1052-4f0c-999b-881a74a94549
ms.date: 12/05/2018
ms.keywords: '*PCERT_VIEWPROPERTIES_STRUCT_A, CERT_VIEWPROPERTIES_STRUCT, CERT_VIEWPROPERTIES_STRUCT structure [Security], CERT_VIEWPROPERTIES_STRUCT_A, CM_ADD_CERT_STORES, CM_ENABLEHOOK, CM_ENABLETEMPLATE, CM_HIDE_ADVANCEPAGE, CM_HIDE_DETAILPAGE, CM_HIDE_TRUSTPAGE, CM_NO_EDITTRUST, CM_NO_NAMECHANGE, CM_SHOW_HELP, CM_SHOW_HELPICON, PCERT_VIEWPROPERTIES_STRUCT, PCERT_VIEWPROPERTIES_STRUCT structure pointer [Security], cryptdlg/CERT_VIEWPROPERTIES_STRUCT, cryptdlg/PCERT_VIEWPROPERTIES_STRUCT, security.cert_viewproperties_struct'
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: CERT_VIEWPROPERTIES_STRUCT_A, *PCERT_VIEWPROPERTIES_STRUCT_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCERT_VIEWPROPERTIES_STRUCT_A
 - cryptdlg/tagCERT_VIEWPROPERTIES_STRUCT_A
 - PCERT_VIEWPROPERTIES_STRUCT_A
 - cryptdlg/PCERT_VIEWPROPERTIES_STRUCT_A
 - CERT_VIEWPROPERTIES_STRUCT_A
 - cryptdlg/CERT_VIEWPROPERTIES_STRUCT_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CryptDlg.h
api_name:
 - CERT_VIEWPROPERTIES_STRUCT
 - cert_viewproperties_struct_a
---

# CERT_VIEWPROPERTIES_STRUCT_A structure


## -description

<p class="CCE_Message">[The  <b>CERT_VIEWPROPERTIES_STRUCT</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CERT_VIEWPROPERTIES_STRUCT</b> structure defines information used when  the <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certviewpropertiesa">CertViewProperties</a> function  is called to display a certificate's properties.

## -struct-fields

### -field dwSize

The size, in bytes, of this structure.

### -field hwndParent

A handle to the parent window.

### -field hInstance

A handle to the module instance.

### -field dwFlags

Bitwise combination of zero or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CM_ENABLEHOOK"></a><a id="cm_enablehook"></a><dl>
<dt><b>CM_ENABLEHOOK</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies that a hook function is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_SHOW_HELP"></a><a id="cm_show_help"></a><dl>
<dt><b>CM_SHOW_HELP</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Specifies that a help file is used.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_SHOW_HELPICON"></a><a id="cm_show_helpicon"></a><dl>
<dt><b>CM_SHOW_HELPICON</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
Specifies that a help icon is used.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_ENABLETEMPLATE"></a><a id="cm_enabletemplate"></a><dl>
<dt><b>CM_ENABLETEMPLATE</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
Specifies that a template is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_HIDE_ADVANCEPAGE"></a><a id="cm_hide_advancepage"></a><dl>
<dt><b>CM_HIDE_ADVANCEPAGE</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Specifies that the <b>Advance</b> tab is not displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_HIDE_TRUSTPAGE"></a><a id="cm_hide_trustpage"></a><dl>
<dt><b>CM_HIDE_TRUSTPAGE</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
Specifies that the <b>Trust</b> tab is not displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_NO_NAMECHANGE"></a><a id="cm_no_namechange"></a><dl>
<dt><b>CM_NO_NAMECHANGE</b></dt>
<dt>64 (0x40)</dt>
</dl>
</td>
<td width="60%">
Specifies that the name cannot be changed.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_NO_EDITTRUST"></a><a id="cm_no_edittrust"></a><dl>
<dt><b>CM_NO_EDITTRUST</b></dt>
<dt>128 (0x80)</dt>
</dl>
</td>
<td width="60%">
Specifies that the trust cannot be edited.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_HIDE_DETAILPAGE"></a><a id="cm_hide_detailpage"></a><dl>
<dt><b>CM_HIDE_DETAILPAGE</b></dt>
<dt>256 (0x100)</dt>
</dl>
</td>
<td width="60%">
Specifies that the <b>Detail</b> tab is not displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="CM_ADD_CERT_STORES"></a><a id="cm_add_cert_stores"></a><dl>
<dt><b>CM_ADD_CERT_STORES</b></dt>
<dt>512 (0x200)</dt>
</dl>
</td>
<td width="60%">
Specifies that certificate stores are opened.

</td>
</tr>
</table>

### -field szTitle

A pointer to a null-terminated string for the title of the user interface.

### -field pCertContext

Certificate context for the certificate to be shown.

### -field arrayPurposes

A pointer to an array of null-terminated strings that specify the certificate purposes.

### -field cArrayPurposes

Number of elements in the <b>arrayPurposes</b> array. If this value is zero, then no trust status is displayed.

### -field cRootStores

Number of elements in the <b>rghstoreRoots</b> array.

### -field rghstoreRoots

Array of Root certificate store handles.

### -field cStores

Number of elements in the <b>rghstoreCAs</b> array.

### -field rghstoreCAs

Array of other certificate store handles.

### -field cTrustStores

Number of elements in the <b>rghstoreTrust</b> array.

### -field rghstoreTrust

Array of trust certificate store handles.

### -field hprov

A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to use for verification.

### -field lCustData

Value used for custom data.

### -field dwPad

Padding location.

### -field szHelpFileName

A pointer to a null-terminated string for the Help file name.

### -field dwHelpId

ID for the Help file topic.

### -field nStartPage

Number of the first property page.

### -field cArrayPropSheetPages

Number of elements in the <b>arrayPropSheetPages</b> array.

### -field arrayPropSheetPages

A pointer to an array of <b>PROPSHEETPAGE</b> structures that specify the property pages.

## -see-also

<a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certviewpropertiesa">CertViewProperties</a>

## -remarks

> [!NOTE]
> The cryptdlg.h header defines CERT_VIEWPROPERTIES_STRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
