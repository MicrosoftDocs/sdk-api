---
UID: NS:commctrl.tagTBSAVEPARAMSA
title: tagTBSAVEPARAMSA
author: windows-sdk-content
description: Specifies the location in the registry where the TB_SAVERESTORE message stores and retrieves information about the state of a toolbar.
old-location: controls\TBSAVEPARAMS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbsaveparams.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPTBSAVEPARAMSA, TBSAVEPARAMS, TBSAVEPARAMS structure [Windows Controls], TBSAVEPARAMSA, TBSAVEPARAMSW, _win32_TBSAVEPARAMS, _win32_TBSAVEPARAMS_cpp, commctrl/TBSAVEPARAMS, commctrl/TBSAVEPARAMSA, commctrl/TBSAVEPARAMSW, controls.TBSAVEPARAMS, controls._win32_TBSAVEPARAMS, tagTBSAVEPARAMSA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TBSAVEPARAMSW (Unicode) and TBSAVEPARAMSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBSAVEPARAMS
 - TBSAVEPARAMSA
 - TBSAVEPARAMSW
product: Windows
targetos: Windows
req.typenames: TBSAVEPARAMSA, *LPTBSAVEPARAMSA
req.redist: 
---

# tagTBSAVEPARAMSA structure


## -description


Specifies the location in the registry where the <a href="https://msdn.microsoft.com/en-us/library/Bb787394(v=VS.85).aspx">TB_SAVERESTORE</a> message stores and retrieves information about the state of a toolbar. 


## -struct-fields




### -field hkr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HKEY</a></b>

Handle to the registry key. 


### -field pszSubKey

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

Subkey name. 


### -field pszValueName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

Value name. 

