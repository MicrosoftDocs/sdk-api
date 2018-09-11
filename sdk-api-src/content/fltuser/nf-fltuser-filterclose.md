---
UID: NF:fltuser.FilterClose
title: FilterClose function
author: windows-sdk-content
description: The FilterClose function closes an open minifilter handle.
old-location: ifsk\filterclose.htm
tech.root: ifsk
ms.assetid: c5d3774e-6f57-4a6b-97a8-623268884859
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: FilterClose, FilterClose function [Installable File System Drivers], FltWin32ApiRef_42f7f157-b74a-4856-ac99-bca1caac3493.xml, fltuser/FilterClose, ifsk.filterclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FilterClose function


## -description


The <b>FilterClose</b> function closes an open minifilter handle. 


## -parameters




### -param hFilter [in]

Minifilter handle returned by a previous call to <a href="https://msdn.microsoft.com/950e0b5b-4ee3-4eed-9039-823a6942cd38">FilterCreate</a>. 


## -returns



<b>FilterClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After <b>FilterClose</b> is called, the minifilter handle that the <i>hFilter</i> parameter specifies is no longer valid and cannot safely be used. 

Use <b>FilterClose</b> to close open minifilter handles returned by calls to <a href="https://msdn.microsoft.com/950e0b5b-4ee3-4eed-9039-823a6942cd38">FilterCreate</a>. Use <a href="https://msdn.microsoft.com/053c06b0-3bfd-436c-ab98-14c55e66da53">FilterFindClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/e6a7c5a2-838d-47b1-ab16-aa1d27806f53">FilterFindFirst</a>. 

To close a connection port handle that was opened by calling <a href="https://msdn.microsoft.com/294783f2-2cbf-4eea-82ae-a396c62f911a">FilterConnectCommunicationPort</a>, use <a href="http://go.microsoft.com/fwlink/p/?linkid=139078">CloseHandle</a>. 




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=139078">CloseHandle</a>



<a href="https://msdn.microsoft.com/294783f2-2cbf-4eea-82ae-a396c62f911a">FilterConnectCommunicationPort</a>



<a href="https://msdn.microsoft.com/950e0b5b-4ee3-4eed-9039-823a6942cd38">FilterCreate</a>



<a href="https://msdn.microsoft.com/053c06b0-3bfd-436c-ab98-14c55e66da53">FilterFindClose</a>



<a href="https://msdn.microsoft.com/e6a7c5a2-838d-47b1-ab16-aa1d27806f53">FilterFindFirst</a>
 

 

