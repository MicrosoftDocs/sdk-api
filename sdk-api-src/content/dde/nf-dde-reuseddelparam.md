---
UID: NF:dde.ReuseDDElParam
title: ReuseDDElParam function
author: windows-sdk-content
description: Enables an application to reuse a packed Dynamic Data Exchange (DDE) lParam parameter, rather than allocating a new packed lParam. Using this function reduces reallocations for applications that pass packed DDE messages.
old-location: dataxchg\reuseddelparam.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\reuseddelparam.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ReuseDDElParam, ReuseDDElParam function [Data Exchange], _win32_ReuseDDElParam, _win32_reuseddelparam_cpp, dataxchg.reuseddelparam, dde/ReuseDDElParam, winui._win32_reuseddelparam
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
api_name:
 - ReuseDDElParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReuseDDElParam function


## -description


Enables an application to reuse a packed Dynamic Data Exchange (DDE) <i>lParam</i> parameter, rather than allocating a new packed 
			<i>lParam</i>. Using this function reduces reallocations for applications that pass packed DDE messages. 


## -parameters




### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message being reused. 


### -param msgIn [in]

Type: <b>UINT</b>

The identifier of the received DDE message. 


### -param msgOut [in]

Type: <b>UINT</b>

The identifier of the DDE message to be posted. The DDE message will reuse the packed 
					<i>lParam</i> parameter. 


### -param uiLo [in]

Type: <b>UINT_PTR</b>

The value to be packed into the low-order word of the reused 
					<i>lParam</i> parameter. 


### -param uiHi [in]

Type: <b>UINT_PTR</b>

The value to be packed into the high-order word of the reused 
					<i>lParam</i> parameter. 


## -returns



Type: <b>LPARAM</b>

The return value is the new 
						<i>lParam</i> value. 




## -remarks



The return value must be posted as the 
				<i>lParam</i> parameter of a DDE message; it must not be used for any other purpose. Once the return value is posted, the posting application need not perform any action to dispose of the 
				<i>lParam</i> parameter. 

Use <b>ReuseDDElParam</b> instead of <a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a> if the 
				<i>lParam</i> parameter will be reused in a responding message. <b>ReuseDDElParam</b> returns the 
				<i>lParam</i> appropriate for reuse. 

This function allocates or frees 
				<i>lParam</i> parameters as needed, depending on the packing requirements of the incoming and outgoing messages. This reduces reallocations in passing DDE messages. 




## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a>



<a href="https://msdn.microsoft.com/9131229d-2515-40d2-a4a8-4c8f7987ac09">PackDDElParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a7da276f-0e29-4abc-86cf-ac1fd23d84b0">UnpackDDElParam</a>
 

 

