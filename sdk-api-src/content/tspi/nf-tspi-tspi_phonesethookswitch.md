---
UID: NF:tspi.TSPI_phoneSetHookSwitch
title: TSPI_phoneSetHookSwitch function
author: windows-sdk-content
description: The TSPI_phoneSetHookSwitch function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.
old-location: tspi\tspi_phonesethookswitch.htm
tech.root: tapi
ms.assetid: e0cfe1b7-9904-4baf-8801-43bc1a5d05d8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_phoneSetHookSwitch, TSPI_phoneSetHookSwitch function [TAPI 2.2], _tspi_tspi_phonesethookswitch, tspi.tspi_phonesethookswitch, tspi/TSPI_phoneSetHookSwitch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tspi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneSetHookSwitch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneSetHookSwitch function


## -description


The 
<b>TSPI_phoneSetHookSwitch</b> function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdPhone

The handle to the phone containing the hookswitch devices whose modes are to be set.


### -param dwHookSwitchDevs

The device(s) whose hookswitch mode is to be set. This parameter uses one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ constants</a>.


### -param dwHookSwitchMode

The hookswitch mode to set. This parameter can have only one of the 
<a href="https://msdn.microsoft.com/532bf089-d5ca-4a04-847d-69e48990ff5c">PHONEHOOKSWITCHMODE_ constants</a>.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALHOOKSWITCHMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONUNAVAIL.




## -remarks



The hookswitch mode is changed to the indicated setting for all devices specified. If different settings are desired, this function can be invoked multiple times with a different set of parameters. A 
<a href="https://msdn.microsoft.com/4772e24c-cafb-4fda-8243-5117c9a73753">PHONE_STATE</a> message is sent to the application after the hookswitch state has changed.




## -see-also




<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>



<a href="https://msdn.microsoft.com/532bf089-d5ca-4a04-847d-69e48990ff5c">PHONEHOOKSWITCHMODE_ Constants</a>



<a href="https://msdn.microsoft.com/798a6c57-d3d3-4924-a925-059de350d18e">PHONESTATUS</a>



<a href="https://msdn.microsoft.com/4772e24c-cafb-4fda-8243-5117c9a73753">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/31248a74-84f2-4ca6-a6fc-f8710953ce34">TSPI_phoneGetHookSwitch</a>
 

 

