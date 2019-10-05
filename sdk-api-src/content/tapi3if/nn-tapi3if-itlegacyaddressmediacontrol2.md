---
UID: NN:tapi3if.ITLegacyAddressMediaControl2
title: ITLegacyAddressMediaControl2 (tapi3if.h)
author: windows-sdk-content
description: The ITLegacyAddressMediaControl2 interface derives from the ITLegacyAddressMediaControl interface. ITLegacyAddressMediaControl2 provides additional methods that allow the configuration of parameters related to line devices.
old-location: tapi3\itlegacyaddressmediacontrol2.htm
tech.root: Tapi
ms.assetid: 38e5f1ba-b31e-47c9-a24a-2e4d37a0961b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITLegacyAddressMediaControl2, ITLegacyAddressMediaControl2 interface [TAPI 2.2], ITLegacyAddressMediaControl2 interface [TAPI 2.2],described, _tapi3_itlegacyaddressmediacontrol2, tapi3.itlegacyaddressmediacontrol2, tapi3if/ITLegacyAddressMediaControl2
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITLegacyAddressMediaControl2"
dev_langs:
 - c++
req.header: tapi3if.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyAddressMediaControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyAddressMediaControl2 interface


## -description


The 
<b>ITLegacyAddressMediaControl2</b> interface derives from the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a> interface. 
<b>ITLegacyAddressMediaControl2</b> provides additional methods that allow the configuration of parameters related to line devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyAddressMediaControl2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITLegacyAddressMediaControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyAddressMediaControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol2-configdialog">ConfigDialog</a>
</td>
<td align="left" width="63%">
Displays a dialog box to allow the user to configure parameters related to the specified line device. The parameters that can be edited are those currently in use on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol2-configdialogedit">ConfigDialogEdit</a>
</td>
<td align="left" width="63%">
Displays a dialog box to allow the user to configure parameters related to the specified line device. The parameters to edit are passed in from the application, and the results are returned to the application.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>
 

 

