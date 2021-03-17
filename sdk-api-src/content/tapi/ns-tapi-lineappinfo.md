---
UID: NS:tapi.lineappinfo_tag
title: LINEAPPINFO (tapi.h)
description: The LINEAPPINFO structure contains information about the application that is currently running. The LINEDEVSTATUS structure can contain an array of LINEAPPINFO structures.
helpviewer_keywords: ["*LPLINEAPPINFO","LINEAPPINFO","LINEAPPINFO structure [TAPI 2.2]","LPLINEAPPINFO","LPLINEAPPINFO structure pointer [TAPI 2.2]","_tapi2_lineappinfo_str","tapi/LINEAPPINFO","tapi/LPLINEAPPINFO","tapi2.lineappinfo_str"]
old-location: tapi2\lineappinfo_str.htm
tech.root: tapi3
ms.assetid: 1c1d2d31-a234-407e-b9fc-4823928c5ca1
ms.date: 12/05/2018
ms.keywords: '*LPLINEAPPINFO, LINEAPPINFO, LINEAPPINFO structure [TAPI 2.2], LPLINEAPPINFO, LPLINEAPPINFO structure pointer [TAPI 2.2], _tapi2_lineappinfo_str, tapi/LINEAPPINFO, tapi/LPLINEAPPINFO, tapi2.lineappinfo_str'
req.header: tapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINEAPPINFO, *LPLINEAPPINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineappinfo_tag
 - tapi/lineappinfo_tag
 - LPLINEAPPINFO
 - tapi/LPLINEAPPINFO
 - LINEAPPINFO
 - tapi/LINEAPPINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAPPINFO
---

# LINEAPPINFO structure


## -description

The 
<b>LINEAPPINFO</b> structure contains information about the application that is currently running. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure can contain an array of 
<b>LINEAPPINFO</b> structures.

## -struct-fields

### -field dwMachineNameSize

Size of the computer name string including the <b>null</b> terminator, in bytes.

### -field dwMachineNameOffset

Offset from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure to a string specifying the name of the computer on which the application is executing. The size of the field is specified by <b>dwMachineNameSize</b>.

### -field dwUserNameSize

Size of the user name string including the <b>null</b> terminator, in bytes.

### -field dwUserNameOffset

Offset from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure to a string specifying the user name under whose account the application is running. The size of the field is specified by <b>dwUserNameSize</b>.

### -field dwModuleFilenameSize

Size of the module file name string, in bytes.

### -field dwModuleFilenameOffset

Offset from the beginning of 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> to a string specifying the module file name of the application. This string can be used in a call to 
<a href="/windows/desktop/api/tapi/nf-tapi-linehandoff">lineHandoff</a> to perform a directed handoff to the application. The size of the field is specified by <b>dwModuleFilenameSize</b>.

### -field dwFriendlyNameSize

Size of the display name string, in bytes.

### -field dwFriendlyNameOffset

Offset from the beginning of 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> to the string provided by the application to 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>, which should be used in any display to the user. The size of the field is specified by <b>dwFriendlyNameSize</b>.

### -field dwMediaModes

Media types for which the application has requested ownership of new calls; zero if when it opened the line <b>dwPrivileges</b> did not include LINECALLPRIVILEGE_OWNER.

### -field dwAddressID

If the line handle was opened using LINEOPENOPTION_SINGLEADDRESS, contains the address identifier specified; set to 0xFFFFFFFF if the single address option was not used. 




An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetlinedevstatus">TSPI_lineGetLineDevStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linehandoff">lineHandoff</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>