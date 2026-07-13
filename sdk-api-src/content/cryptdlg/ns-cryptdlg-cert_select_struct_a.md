---
UID: NS:cryptdlg.tagCSSA
title: CERT_SELECT_STRUCT_A (cryptdlg.h)
description: Contains criteria upon which to select certificates that are presented in a certificate selection dialog box. This structure is used in the CertSelectCertificate function. (ANSI)
helpviewer_keywords: ["*PCERT_SELECT_STRUCT_A","CERT_SELECT_STRUCT","CERT_SELECT_STRUCT structure [Security]","CERT_SELECT_STRUCT_A","CERT_SELECT_STRUCT_W","CSS_ALLOWMULTISELECT","CSS_ENABLEHOOK","CSS_ENABLETEMPLATE","CSS_ENABLETEMPLATEHANDLE","CSS_HIDE_PROPERTIES","CSS_SHOW_HELP","PCERT_SELECT_STRUCT","PCERT_SELECT_STRUCT structure pointer [Security]","cryptdlg/CERT_SELECT_STRUCT","cryptdlg/CERT_SELECT_STRUCT_A","cryptdlg/CERT_SELECT_STRUCT_W","cryptdlg/PCERT_SELECT_STRUCT","security.cert_select_struct","security.cert_select_struct_w"]
old-location: security\cert_select_struct.htm
tech.root: security
ms.assetid: 49184872-d636-4e55-8e32-0f38b49b5c21
ms.date: 12/05/2018
ms.keywords: '*PCERT_SELECT_STRUCT_A, CERT_SELECT_STRUCT, CERT_SELECT_STRUCT structure [Security], CERT_SELECT_STRUCT_A, CERT_SELECT_STRUCT_W, CSS_ALLOWMULTISELECT, CSS_ENABLEHOOK, CSS_ENABLETEMPLATE, CSS_ENABLETEMPLATEHANDLE, CSS_HIDE_PROPERTIES, CSS_SHOW_HELP, PCERT_SELECT_STRUCT, PCERT_SELECT_STRUCT structure pointer [Security], cryptdlg/CERT_SELECT_STRUCT, cryptdlg/CERT_SELECT_STRUCT_A, cryptdlg/CERT_SELECT_STRUCT_W, cryptdlg/PCERT_SELECT_STRUCT, security.cert_select_struct, security.cert_select_struct_w'
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CERT_SELECT_STRUCT_W (Unicode) and CERT_SELECT_STRUCT_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CERT_SELECT_STRUCT_A, *PCERT_SELECT_STRUCT_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSSA
 - cryptdlg/tagCSSA
 - PCERT_SELECT_STRUCT_A
 - cryptdlg/PCERT_SELECT_STRUCT_A
 - CERT_SELECT_STRUCT_A
 - cryptdlg/CERT_SELECT_STRUCT_A
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
 - CERT_SELECT_STRUCT
 - CERT_SELECT_STRUCT_A
 - CERT_SELECT_STRUCT_W
---

# CERT_SELECT_STRUCT_A structure


## -description

The <b>CERT_SELECT_STRUCT</b> structure 
    contains criteria upon  which to select certificates that are presented in a certificate selection 
    dialog box.  This structure is used in the 
    <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> 
    function.

## -struct-fields

### -field dwSize

The size, in bytes, of this structure.

### -field hwndParent

A handle to the parent window of any dialog boxes that 
      <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> generates.

### -field hInstance

A handle to the module whose executable file contains the dialog box template.

### -field pTemplateName

If the <b>CSS_ENABLETEMPLATE</b> flag is set in the <b>dwFlags</b> 
      member, set <b>pTemplateName</b> to a pointer to a global memory object that contains the 
      template that <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a> 
      uses to create the dialog box. A dialog box template consists of a header that describes the dialog box. The 
      header is followed by one or more additional blocks of data that describe each of the controls in the dialog 
      box. The template can use either the standard format or the extended format.
      

If the <b>CSS_ENABLETEMPLATEHANDLE</b> flag is set in <b>dwFlags</b>, 
       <b>pTemplateName</b> specifies the dialog box template. 
       <b>pTemplateName</b> is either the pointer to a null-terminated character string that 
       specifies the name of the dialog box template or an integer value that specifies the resource identifier of the 
       dialog box template. If the  specifies a resource identifier, its high-order word must be zero and its 
       low-order word must contain the identifier. One way to create this integer value is to use the 
       <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro.

### -field dwFlags

This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSS_HIDE_PROPERTIES"></a><a id="css_hide_properties"></a><dl>
<dt><b>CSS_HIDE_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
Hide the <b>Properties</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="CSS_ENABLEHOOK"></a><a id="css_enablehook"></a><dl>
<dt><b>CSS_ENABLEHOOK</b></dt>
</dl>
</td>
<td width="60%">
Pass a hook procedure in <b>pfnHook</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CSS_ALLOWMULTISELECT"></a><a id="css_allowmultiselect"></a><dl>
<dt><b>CSS_ALLOWMULTISELECT</b></dt>
</dl>
</td>
<td width="60%">
Enable multi-selection of certificates. This option is not currently supported and is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="CSS_SHOW_HELP"></a><a id="css_show_help"></a><dl>
<dt><b>CSS_SHOW_HELP</b></dt>
</dl>
</td>
<td width="60%">
Show the <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="CSS_ENABLETEMPLATE"></a><a id="css_enabletemplate"></a><dl>
<dt><b>CSS_ENABLETEMPLATE</b></dt>
</dl>
</td>
<td width="60%">
Cause <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> 
        function to call the 
        <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a> function to 
        create a dialog box. For more information, see <b>pTemplateName</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CSS_ENABLETEMPLATEHANDLE"></a><a id="css_enabletemplatehandle"></a><dl>
<dt><b>CSS_ENABLETEMPLATEHANDLE</b></dt>
</dl>
</td>
<td width="60%">
Cause the <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> 
        function to call the <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxparama">DialogBoxParam</a> function 
        to create a dialog box. For more information, see <b>pTemplateName</b>.

</td>
</tr>
</table>

### -field szTitle

A pointer to a string that contains the text for the title of the dialog box.

### -field cCertStore

The number of elements in <b>arrayCertStore</b> array.

### -field arrayCertStore

A pointer to the array of certificate stores that the dialog box enumerates and displays the certificates 
      from. The <b>cCertStore</b> member contains the number of elements in this array.

### -field szPurposeOid

A pointer to a string representation of an object identifier (OID) for an enhanced key usage (EKU). If an 
      OID is provided, only certificates that include this EKU will be displayed.

### -field cCertContext

The number of elements in the <b>arrayCertContext</b> array. After the 
      <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function returns, 
      this member contains the number of certificates that were selected by the user. Currently, only one certificate 
      can be selected by the user.

### -field arrayCertContext

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> 
     structures. The <b>cCertContext</b> member specifies the number of elements in this array. 
     This array must contain at least one element.
     

The certificates represented by these structures are selected when the dialog box displayed by the 
      <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function is 
      initially displayed.  Currently, only the first certificate in this array is used. The first certificate in this 
      array will be released with the 
      <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function 
      if the <b>CertSelectCertificate</b> function is 
      successful. If the first element in this array is <b>NULL</b>, no certificates are initially 
      selected in the dialog box.

After the <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function 
      returns, this array contains the certificates that were selected by the user. Currently, only one certificate 
      can be selected by the user.

### -field lCustData

A pointer to an array of byte values that hold custom data that is passed through to the filter procedure 
      referenced by <b>pfnFilter</b>. This custom data is not used by the 
      <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function.

### -field pfnHook

A <a href="/windows/desktop/api/cryptdlg/nc-cryptdlg-pfncmhookproc">PFNCMHOOKPROC</a> function pointer to the Hook 
      callback function. This function is called before messages are processed by the dialog box. For more 
      information, see <a href="/windows/desktop/winmsg/hooks">Hooks</a>.

### -field pfnFilter

A <a href="/windows/desktop/api/cryptdlg/nc-cryptdlg-pfncmfilterproc">PFNCMFILTERPROC</a> function pointer to the 
      filter callback function. This is called to determine which certificates will be displayed by the dialog 
      box.

### -field szHelpFileName

A pointer to a null-terminated string that contains the full path to the Help file.

### -field dwHelpId

The context identifier for the topic. For more information, see  
      <a href="/previous-versions/windows/desktop/htmlhelp/winhelp">WinHelp</a>.

### -field hprov

A handle to the 
      <a href="/windows/desktop/SecCrypto/cryptographic-service-providers">Cryptographic Service Provider</a> (CSP) 
      to use for certificate verification.

## -see-also

<a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a>

## -remarks

> [!NOTE]
> The cryptdlg.h header defines CERT_SELECT_STRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
