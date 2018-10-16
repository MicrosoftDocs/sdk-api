---
UID: NF:dde.UnpackDDElParam
title: UnpackDDElParam function
author: windows-sdk-content
description: Unpacks a Dynamic Data Exchange (DDE)lParam value received from a posted DDE message.
old-location: dataxchg\unpackddelparam.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\unpackddelparam.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: UnpackDDElParam, UnpackDDElParam function [Data Exchange], _win32_UnpackDDElParam, _win32_unpackddelparam_cpp, dataxchg.unpackddelparam, dde/UnpackDDElParam, winui._win32_unpackddelparam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dde.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-L1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-3-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - UnpackDDElParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnpackDDElParam function


## -description


Unpacks a Dynamic Data Exchange (DDE)<i>lParam</i> value received from a posted DDE message. 


## -parameters




### -param msg [in]

Type: <b>UINT</b>

The posted DDE message. 


### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message that was received. The application must free the memory object specified by the 
					<i>lParam</i> parameter by calling the <a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a> function. 


### -param puiLo [out]

Type: <b>PUINT_PTR</b>

A pointer to a variable that receives the low-order word of 
					<i>lParam</i>. 


### -param puiHi [out]

Type: <b>PUINT_PTR</b>

A pointer to a variable that receives the high-order word of 
					<i>lParam</i>. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks




<a href="https://msdn.microsoft.com/9131229d-2515-40d2-a4a8-4c8f7987ac09">PackDDElParam</a> eases the porting of 16-bit DDE applications to 32-bit DDE applications. 




## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a>



<a href="https://msdn.microsoft.com/9131229d-2515-40d2-a4a8-4c8f7987ac09">PackDDElParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/069ac8ee-3d92-4969-8c6b-78a8a0c76721">ReuseDDElParam</a>
 

 

