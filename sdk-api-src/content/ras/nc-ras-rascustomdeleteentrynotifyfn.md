---
UID: NC:ras.RasCustomDeleteEntryNotifyFn
title: RasCustomDeleteEntryNotifyFn (ras.h)
description: The RasCustomDeleteEntryNotify function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.
helpviewer_keywords: ["RCD_AllUsers","RCD_Eap","RCD_Logon","RCD_SingleUser","RasCustomDeleteEntryNotify","RasCustomDeleteEntryNotify callback function [RAS]","RasCustomDeleteEntryNotifyFn","RasCustomDeleteEntryNotifyFn callback","_ras_rascustomdeleteentrynotify","ras/RasCustomDeleteEntryNotify","rras.rascustomdeleteentrynotify"]
old-location: rras\rascustomdeleteentrynotify.htm
tech.root: RRAS
ms.assetid: bbdaff05-ec86-461a-b466-8f69cb9cba5a
ms.date: 12/05/2018
ms.keywords: RCD_AllUsers, RCD_Eap, RCD_Logon, RCD_SingleUser, RasCustomDeleteEntryNotify, RasCustomDeleteEntryNotify callback function [RAS], RasCustomDeleteEntryNotifyFn, RasCustomDeleteEntryNotifyFn callback, _ras_rascustomdeleteentrynotify, ras/RasCustomDeleteEntryNotify, rras.rascustomdeleteentrynotify
req.header: ras.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasCustomDeleteEntryNotifyFn
 - ras/RasCustomDeleteEntryNotifyFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasCustomDeleteEntryNotify
---

# RasCustomDeleteEntryNotifyFn callback function


## -description

The 
<i>RasCustomDeleteEntryNotify</i> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.

## -parameters

### -param lpszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param lpszEntry [in]

Pointer to a <b>null</b>-terminated string that contains the name of the phone-book entry to dial.

### -param dwFlags [in]

Specifies one or more of the following flags: 



						
						
					



#### RCD_SingleUser (0x00000000)



#### RCD_AllUsers (0x00000001)



#### RCD_Eap (0x00000002)



#### RCD_Logon (0x00000004)

## -returns

This function should return value <b>ERROR_SUCCESS</b> if successful.

## -see-also

<a href="/windows/desktop/RRAS/custom-dialers">Custom Dialers</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomdialfn">RasCustomDial</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomdialdlgfn">RasCustomDialDlg</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomentrydlgfn">RasCustomEntryDlg</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomhangupfn">RasCustomHangUp</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>