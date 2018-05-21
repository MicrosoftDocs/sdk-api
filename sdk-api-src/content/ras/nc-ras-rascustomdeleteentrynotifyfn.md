---
UID: NC:ras.RasCustomDeleteEntryNotifyFn
title: RasCustomDeleteEntryNotifyFn
author: windows-driver-content
description: The RasCustomDeleteEntryNotify function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.
old-location: rras\rascustomdeleteentrynotify.htm
old-project: RRAS
ms.assetid: bbdaff05-ec86-461a-b466-8f69cb9cba5a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: RCD_AllUsers, RCD_Eap, RCD_Logon, RCD_SingleUser, RasCustomDeleteEntryNotify, RasCustomDeleteEntryNotify callback function [RAS], RasCustomDeleteEntryNotifyFn, RasCustomDeleteEntryNotifyFn callback, _ras_rascustomdeleteentrynotify, ras/RasCustomDeleteEntryNotify, rras.rascustomdeleteentrynotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ras.h
api_name:
-	RasCustomDeleteEntryNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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




<a href="https://msdn.microsoft.com/ad94f38d-812f-4329-8055-6274a21a3242">Custom Dialers</a>



<a href="https://msdn.microsoft.com/8c3f807b-3e31-4ce6-8549-74ab06cbba7f">RasCustomDial</a>



<a href="https://msdn.microsoft.com/d1f4715a-a31c-4346-ac0a-83f2c58e8cc1">RasCustomDialDlg</a>



<a href="https://msdn.microsoft.com/4778069b-87d0-4379-95f7-718fe0d7a56c">RasCustomEntryDlg</a>



<a href="https://msdn.microsoft.com/56410af3-7b23-4536-998d-88d78d45585d">RasCustomHangUp</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

