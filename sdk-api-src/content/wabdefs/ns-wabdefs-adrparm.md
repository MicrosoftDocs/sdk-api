---
UID: NS:wabdefs._ADRPARM
title: ADRPARM (wabdefs.h)
description: Do not use. Describes the display and behavior of the common address dialog box.
helpviewer_keywords: ["*LPADRPARM","AB_RESOLVE","AB_SELECTONLY","ADDRESS_ONE","ADRPARM","ADRPARM structure [Windows Address Book]","DIALOG_MODAL","DIALOG_SDI","LPADRPARM","LPADRPARM structure pointer [Windows Address Book]","_wab_ADRPARM","wab._wab_ADRPARM","wabdefs/ADRPARM","wabdefs/LPADRPARM"]
old-location: wab\_wab_ADRPARM.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\adrparm.htm
ms.date: 12/05/2018
ms.keywords: '*LPADRPARM, AB_RESOLVE, AB_SELECTONLY, ADDRESS_ONE, ADRPARM, ADRPARM structure [Windows Address Book], DIALOG_MODAL, DIALOG_SDI, LPADRPARM, LPADRPARM structure pointer [Windows Address Book], _wab_ADRPARM, wab._wab_ADRPARM, wabdefs/ADRPARM, wabdefs/LPADRPARM'
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ADRPARM, *LPADRPARM
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _ADRPARM
 - wabdefs/_ADRPARM
 - LPADRPARM
 - wabdefs/LPADRPARM
 - ADRPARM
 - wabdefs/ADRPARM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - ADRPARM
---

# ADRPARM structure


## -description

Do not use. Describes the display and behavior of the common address dialog box.

## -struct-fields

### -field cbABContEntryID

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the list of entries that can be added to the recipient wells.

### -field lpABContEntryID

Type: <b>LPENTRYID</b>

Pointer to a variable of type <a href="/previous-versions/windows/desktop/api/wabdefs/ns-wabdefs-entryid">ENTRYID</a> that specifies the container that will supply the list of <a href="/windows/win32/api/wabiab/nf-wabiab-iaddrbook-createoneoff">one-off</a> entries that can be added to the recipient wells of the address book's common dialog box. The address book container that <b>lpABContEntryID</b> points to determines what is listed in the edit box within the dialog box that holds possible recipient names. Usually, <b>lpABContEntryID</b> is <b>NULL</b>, indicating the use of a custom recipient provider.

### -field ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies the bitmask of flags associated with various address dialog box options. The following flags can be set in the WAB.



#### AB_RESOLVE

Causes all names to be resolved after the address book dialog box is closed. The Resolve Name dialog box is displayed if there are ambiguous entries in the recipient list.



#### AB_SELECTONLY

Disables the creation of custom recipient addresses and direct type-in entries for a recipient list. This flag is used only if the dialog box is modal.



#### ADDRESS_ONE

Indicates that the user of the dialog box can select exactly one message recipient, instead of a number of recipients from a recipient list. This flag is valid only when <b>cDestFields</b> is zero. This flag is used only if the dialog box is modal.



#### DIALOG_MODAL

Causes a modal dialog box to be displayed. The client must set either this flag or <b>DIALOG_SDI</b>, but not both.



#### DIALOG_SDI

Causes a modeless dialog box to be displayed. This call returns immediately and thus does not modify the <a href="/windows/desktop/api/wabdefs/ns-wabdefs-adrlist">ADRLIST</a> structure passed in. The caller must set either this flag or <b>DIALOG_MODAL</b>, but not both.

### -field lpReserved

Type: <b>LPVOID</b>

### -field ulHelpContext

Type: <b>ULONG</b>

Not supported. Must be set to 0.

### -field lpszHelpFileName

Type: <b>LPTSTR</b>

Not supported. Must be set to <b>NULL</b>.

### -field lpfnABSDI

Type: <b>LPFNABSDI</b>

Pointer to a WAB function based on the <a href="/previous-versions/office/developer/office-2007/cc839835(v=office.12)">ACCELERATEABSDI</a> prototype (see MAPI documentation), or <b>NULL</b>. This member applies only to the modeless version of the dialog box, as indicated by the <b>DIALOG_SDI</b> flag being set.

Clients building an <b>ADRPARM</b> structure to pass to <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-address-vb">Address</a> must always set the <b>lpfnABSDI</b> member to <b>NULL</b>. If the <b>DIALOG_SDI</b> flag is set, WAB then sets it to a valid function before returning. Clients call this function from within their message loop to ensure that accelerators in the address book dialog box work. When the dialog box is dismissed and WAB calls the function to which the <b>lpfnDismiss</b> member points, clients should unhook the <a href="/previous-versions/office/developer/office-2007/cc839835(v=office.12)">ACCELERATEABSDI</a> function from their message loop.

### -field lpfnDismiss

Type: <b>LPFNDISMISS</b>

Pointer to a function based on the <a href="/previous-versions/office/developer/office-2007/cc815796(v=office.12)">DISMISSMODELESS</a> (see MAPI documentation) prototype, or <b>NULL</b>. This member applies only to the modeless version of the dialog box, as indicated by the <b>DIALOG_SDI</b> flag being set. WAB calls the DISMISSMODELESS function when the user dismisses the modeless address dialog box, informing a client calling <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-address-vb">Address</a> that the dialog box is no longer active.

### -field lpvDismissContext

Type: <b>LPVOID</b>

Pointer to the context information to be passed to the <a href="/previous-versions/office/developer/office-2007/cc815796(v=office.12)">DISMISSMODELESS</a> function to which the <b>lpfnDismiss</b> member points. This member applies only to the modeless version of the dialog box, as indicated by the <b>DIALOG_SDI</b> flag being set.

### -field lpszCaption

Type: <b>LPTSTR</b>

Variable of type <b>LPTSTR</b> that specifies the text to be used as a caption for the address book dialog box.

### -field lpszNewEntryTitle

Type: <b>LPTSTR</b>

Variable of type <b>LPTSTR</b> that specifies the text to be used as a new-entry prompt for an edit box in an address book dialog box.

### -field lpszDestWellsTitle

Type: <b>LPTSTR</b>

Variable of type <b>LPTSTR</b> that specifies the text to be used as a title for the set of recipient-name edit boxes that appears in the dialog box. This member is used only if the address book dialog box is modal.

### -field cDestFields

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of recipient-name edit boxes (that is, destination fields) in the address book dialog box. A number from 0 through 3 is typical. If the <b>cDestFields</b> member is zero and the ADDRESS_ONE flag is not set in <b>ulFlags</b>, the address book will be open for browsing only.

### -field nDestFieldFocus

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the field in the address book dialog box that should have the initial focus when the dialog box appears. This value must be between 0 and the value of <b>cDestFields</b> minus 1.

### -field lppszDestTitles

Type: <b>LPTSTR*</b>

Pointer to an array of variables of type <b>LPTSTR</b> that specify the text titles to be displayed in the recipient-name edit boxes of the address book dialog box. The size of the array is the value of <b>cDestFields</b>. If the <b>lppszDestTitles</b> member is <b>NULL</b>, the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-address-vb">Address</a> method chooses default titles.

### -field lpulDestComps

Type: <b>ULONG*</b>

Pointer to an array of variables of type <b>ULONG</b> that specify the recipient types—such as MAPI_TO, MAPI_CC, and MAPI_BCC—associated with each recipient-name edit box. The size of the array is the value of <b>cDestFields</b>. If the <b>lpulDestComps</b> member is <b>NULL</b>, the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-address-vb">Address</a> method chooses default recipient types.

### -field lpContRestriction

Type: <b>LPSRestriction</b>

Not supported. Must be set to <b>NULL</b>.

### -field lpHierRestriction

Type: <b>LPSRestriction</b>

Not supported. Must be set to <b>NULL</b>.