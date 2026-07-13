---
UID: NF:tapi.lineSetAppPriorityA
title: lineSetAppPriorityA function (tapi.h)
description: Enables an application to set its priority in the handoff priority list for a particular media type or Assisted Telephony request mode, or to remove itself from the priority list. (lineSetAppPriorityA)
helpviewer_keywords: ["lineSetAppPriorityA", "tapi/lineSetAppPriorityA"]
old-location: tapi2\linesetapppriority.htm
tech.root: tapi3
ms.assetid: f173c472-56bc-4773-a77a-1aa05ba8766f
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetapppriority, lineSetAppPriority, lineSetAppPriority function [TAPI 2.2], lineSetAppPriorityA, lineSetAppPriorityW, tapi/lineSetAppPriority, tapi/lineSetAppPriorityA, tapi/lineSetAppPriorityW, tapi2.linesetapppriority
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineSetAppPriorityW (Unicode) and lineSetAppPriorityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetAppPriorityA
 - tapi/lineSetAppPriorityA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetAppPriority
 - lineSetAppPriorityA
 - lineSetAppPriorityW
---

# lineSetAppPriorityA function


## -description

The 
<b>lineSetAppPriority</b> function enables an application to set its priority in the handoff priority list for a particular media type or Assisted Telephony request mode, or to remove itself from the priority list.

## -parameters

### -param lpszAppFilename

A pointer to a string that contains the application executable module filename, without the directory data. In TAPI version 2.0 or later, the parameter can specify a filename in either long or 8.3 filename format.

### -param dwMediaMode

A media type for which the priority of the application is to be set. The value can be one or more of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE</a> constants. The value zero should be used to set the application priority for Assisted Telephony requests.

### -param lpExtensionID

A pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a>. This parameter is ignored.

### -param dwRequestMode

The conditions for this parameter are, if the <i>dwMediaMode</i> parameter is zero, this parameter specifies the Assisted Telephony request mode for which priority is to be set. It must be LINEREQUESTMODE_MAKECALL. This parameter is ignored if <i>dwMediaMode</i> is nonzero.

### -param lpszExtensionName

This parameter is ignored.

### -param dwPriority

A parameter that indicates a new priority for the application. If the value 0 is passed, the application is removed from the priority list for the specified media or request mode; if it was not already present, no error is generated. If the value 1 is passed, the application is inserted as the highest-priority application for the media or request mode; it is removed from a lower-priority position, if already in the list. Any other value generates an error.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

<b>LINEERR_INIFILECORRUPT</b>, <b>LINEERR_INVALREQUESTMODE</b>, <b>LINEERR_INVALAPPNAME</b>, <b>LINEERR_NOMEM</b>, <b>LINEERR_INVALMEDIAMODE</b>, <b>LINEERR_OPERATIONFAILED</b>, <b>LINEERR_INVALPARAM</b>, <b>LINEERR_RESOURCEUNAVAIL</b>, <b>LINEERR_INVALPOINTER</b>.

## -remarks

If <b>LINEERR_INVALMEDIAMODE</b> is returned, the value specified in <i>dwMediaMode</i> is not zero and not one of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>.

This function updates the stored priority list. If the telephony system is initialized, it also sets the current, active priorities for applications then running; the new priority is used on the next incoming call or 
<a href="/windows/desktop/api/tapi/nf-tapi-linehandoff">lineHandoff</a> based on media type.

The Priorities set with <b>lineSetAppPriority</b> will persist across restarts of the system or restarts of tapisrv. The <a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function opens the line with no specified call priorities. By default, the highest priority application will be the one that first called <b>lineOpen</b>.





> [!NOTE]
> The tapi.h header defines lineSetAppPriority as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linehandoff">lineHandoff</a>
