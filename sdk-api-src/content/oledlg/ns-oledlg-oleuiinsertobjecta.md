---
UID: NS:oledlg.tagOLEUIINSERTOBJECTA
title: OLEUIINSERTOBJECTA (oledlg.h)
description: Contains information that the OLE User Interface Library uses to initialize the Insert Object dialog box, and space for the library to return information when the dialog box is dismissed. (ANSI)
helpviewer_keywords: ["*LPOLEUIINSERTOBJECTA","*POLEUIINSERTOBJECTA","IOF_CHECKDISPLAYASICON","IOF_CHECKLINK","IOF_CREATEFILEOBJECT","IOF_CREATELINKOBJECT","IOF_CREATENEWOBJECT","IOF_DISABLEDISPLAYASICON","IOF_DISABLELINK","IOF_HIDECHANGEICON","IOF_SELECTCREATECONTROL","IOF_SELECTCREATEFROMFILE","IOF_SELECTCREATENEW","IOF_SHOWHELP","IOF_SHOWINSERTCONTROL","IOF_VERIFYSERVERSEXIST","LPOLEUIINSERTOBJECT","LPOLEUIINSERTOBJECT structure pointer [COM]","OLEUIINSERTOBJECT","OLEUIINSERTOBJECT structure [COM]","OLEUIINSERTOBJECTA","OLEUIINSERTOBJECTW","POLEUIINSERTOBJECT","POLEUIINSERTOBJECT structure pointer [COM]","_ole_OLEUIINSERTOBJECT_str","com.oleuiinsertobject_struct","oledlg/LPOLEUIINSERTOBJECT","oledlg/OLEUIINSERTOBJECT","oledlg/OLEUIINSERTOBJECTA","oledlg/OLEUIINSERTOBJECTW","oledlg/POLEUIINSERTOBJECT"]
old-location: com\oleuiinsertobject_struct.htm
tech.root: com
ms.assetid: b14df159-ed62-4745-8cac-c31364d0de7b
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIINSERTOBJECTA, *POLEUIINSERTOBJECTA, IOF_CHECKDISPLAYASICON, IOF_CHECKLINK, IOF_CREATEFILEOBJECT, IOF_CREATELINKOBJECT, IOF_CREATENEWOBJECT, IOF_DISABLEDISPLAYASICON, IOF_DISABLELINK, IOF_HIDECHANGEICON, IOF_SELECTCREATECONTROL, IOF_SELECTCREATEFROMFILE, IOF_SELECTCREATENEW, IOF_SHOWHELP, IOF_SHOWINSERTCONTROL, IOF_VERIFYSERVERSEXIST, LPOLEUIINSERTOBJECT, LPOLEUIINSERTOBJECT structure pointer [COM], OLEUIINSERTOBJECT, OLEUIINSERTOBJECT structure [COM], OLEUIINSERTOBJECTA, OLEUIINSERTOBJECTW, POLEUIINSERTOBJECT, POLEUIINSERTOBJECT structure pointer [COM], _ole_OLEUIINSERTOBJECT_str, com.oleuiinsertobject_struct, oledlg/LPOLEUIINSERTOBJECT, oledlg/OLEUIINSERTOBJECT, oledlg/OLEUIINSERTOBJECTA, oledlg/OLEUIINSERTOBJECTW, oledlg/POLEUIINSERTOBJECT'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIINSERTOBJECTW (Unicode) and OLEUIINSERTOBJECTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIINSERTOBJECTA, *POLEUIINSERTOBJECTA, *LPOLEUIINSERTOBJECTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIINSERTOBJECTA
 - oledlg/tagOLEUIINSERTOBJECTA
 - POLEUIINSERTOBJECTA
 - oledlg/POLEUIINSERTOBJECTA
 - OLEUIINSERTOBJECTA
 - oledlg/OLEUIINSERTOBJECTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleDlg.h
api_name:
 - OLEUIINSERTOBJECT
 - OLEUIINSERTOBJECTA
 - OLEUIINSERTOBJECTW
---

# OLEUIINSERTOBJECTA structure


## -description

Contains information that the OLE User Interface Library uses to initialize the <b>Insert Object</b> dialog box, and space for the library to return information when the dialog box is dismissed.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes. This field must be filled on input.

### -field dwFlags

On input, specifies the initialization and creation flags. On exit, specifies the user's choices. It can be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IOF_SHOWHELP"></a><a id="iof_showhelp"></a><dl>
<dt><b>IOF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
The dialog box will display a <b>Help</b> button. 

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_SELECTCREATENEW"></a><a id="iof_selectcreatenew"></a><dl>
<dt><b>IOF_SELECTCREATENEW</b></dt>
</dl>
</td>
<td width="60%">
The <b>Create New</b> radio button will initially be checked. This cannot be used with IOF_SELECTCREATEFROMFILE. 


</td>
</tr>
<tr>
<td width="40%"><a id="IOF_SELECTCREATEFROMFILE"></a><a id="iof_selectcreatefromfile"></a><dl>
<dt><b>IOF_SELECTCREATEFROMFILE</b></dt>
</dl>
</td>
<td width="60%">
The <b>Create From File</b> radio button will initially be checked. This cannot be used with IOF_SELECTCREATENEW. 


</td>
</tr>
<tr>
<td width="40%"><a id="IOF_CHECKLINK"></a><a id="iof_checklink"></a><dl>
<dt><b>IOF_CHECKLINK</b></dt>
</dl>
</td>
<td width="60%">
The <b>Link</b> check box will initially be checked.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_CHECKDISPLAYASICON"></a><a id="iof_checkdisplayasicon"></a><dl>
<dt><b>IOF_CHECKDISPLAYASICON</b></dt>
</dl>
</td>
<td width="60%">
The <b>Display As Icon</b> check box will initially be checked, the current icon will be displayed, and the <b>Change Icon</b> button will be enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_CREATENEWOBJECT"></a><a id="iof_createnewobject"></a><dl>
<dt><b>IOF_CREATENEWOBJECT</b></dt>
</dl>
</td>
<td width="60%">
A new object should be created when the user selects <b>OK</b> to dismiss the dialog box and the <b>Create New</b> radio button was selected.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_CREATEFILEOBJECT"></a><a id="iof_createfileobject"></a><dl>
<dt><b>IOF_CREATEFILEOBJECT</b></dt>
</dl>
</td>
<td width="60%">
A new object should be created from the specified file when the user selects <b>OK</b> to dismiss the dialog box and the <b>Create From File</b> radio button was selected.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_CREATELINKOBJECT"></a><a id="iof_createlinkobject"></a><dl>
<dt><b>IOF_CREATELINKOBJECT</b></dt>
</dl>
</td>
<td width="60%">
 A new linked object should be created when the user selects <b>OK</b> to dismiss the dialog box and the user checked the <b>Link</b> check box. 


</td>
</tr>
<tr>
<td width="40%"><a id="IOF_DISABLELINK"></a><a id="iof_disablelink"></a><dl>
<dt><b>IOF_DISABLELINK</b></dt>
</dl>
</td>
<td width="60%">
 The <b>Link</b> check box will be disabled on initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_VERIFYSERVERSEXIST"></a><a id="iof_verifyserversexist"></a><dl>
<dt><b>IOF_VERIFYSERVERSEXIST</b></dt>
</dl>
</td>
<td width="60%">
The dialog box should validate the classes it adds to the listbox by ensuring that the server specified in the registration database exists. This is a significant performance factor. 


</td>
</tr>
<tr>
<td width="40%"><a id="IOF_DISABLEDISPLAYASICON"></a><a id="iof_disabledisplayasicon"></a><dl>
<dt><b>IOF_DISABLEDISPLAYASICON</b></dt>
</dl>
</td>
<td width="60%">
The <b>Display As Icon</b> check box will be disabled on initialization. 


</td>
</tr>
<tr>
<td width="40%"><a id="IOF_HIDECHANGEICON"></a><a id="iof_hidechangeicon"></a><dl>
<dt><b>IOF_HIDECHANGEICON</b></dt>
</dl>
</td>
<td width="60%">
The <b>Change Icon</b> button will be hidden in the <b>Insert Object</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_SHOWINSERTCONTROL"></a><a id="iof_showinsertcontrol"></a><dl>
<dt><b>IOF_SHOWINSERTCONTROL</b></dt>
</dl>
</td>
<td width="60%">
Displays the <b>Insert Control</b> radio button.

</td>
</tr>
<tr>
<td width="40%"><a id="IOF_SELECTCREATECONTROL"></a><a id="iof_selectcreatecontrol"></a><dl>
<dt><b>IOF_SELECTCREATECONTROL</b></dt>
</dl>
</td>
<td width="60%">
Displays the <b>Create Control</b> radio button.

</td>
</tr>
</table>

### -field hWndOwner

The window that owns the dialog box. This member should not be <b>NULL</b>.

### -field lpszCaption

Pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Insert Object</b>.

### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.

### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member. The library passes a pointer to the <b>OLEUIINSERTOBJECT</b> structure in the <i>lParam</i> parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member.

### -field hInstance

Instance that contains a dialog box template specified by the <b>lpTemplateName</b> member.

### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Insert Object</b> dialog box template.

### -field hResource

Customized template handle.

### -field clsid

CLSID for class of the object to be inserted. Filled on output.

### -field lpszFile

Pointer to the name of the file to be linked or embedded. Filled on output.

### -field cchFile

Size of <b>lpszFile</b> buffer; will not exceed MAX_PATH.

### -field cClsidExclude

Number of CLSIDs included in the <b>lpClsidExclude</b> list. Filled on input.

### -field lpClsidExclude

Pointer to a list of CLSIDs to exclude from listing.

### -field iid

Identifier of the requested interface. If <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> creates the object, then it will return a pointer to this interface. This parameter is ignored if <b>OleUIInsertObject</b> does not create the object.

### -field oleRender

Rendering option. If <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> creates the object, then it selects the rendering option when it creates the object. This parameter is ignored if <b>OleUIInsertObject</b> does not create the object.

### -field lpFormatEtc

Desired format. If <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> creates the object, then it selects the format when it creates the object. This parameter is ignored if <b>OleUIInsertObject</b> does not create the object.

### -field lpIOleClientSite

Pointer to the client site to be used for the object. This parameter is ignored if <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> does not create the object.

### -field lpIStorage

Pointer to the storage to be used for the object. This parameter is ignored if <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> does not create the object.

### -field ppvObj

Address of output pointer variable that contains the interface pointer for the object being inserted. This parameter is ignored if <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> does not create the object.

### -field sc

Result of creation calls. This parameter is ignored if <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a> does not create the object.

### -field hMetaPict

MetafilePict structure containing the iconic aspect, if it wasn't placed in the object's cache.

## -see-also

<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiinsertobjecta">OleUIInsertObject</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIINSERTOBJECT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
