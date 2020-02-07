---
UID: NN:ehstorapi.IEnhancedStorageSilo
title: IEnhancedStorageSilo (ehstorapi.h)
description: IEnhancedStorageSilo interface is the point of access for an IEEE 1667 silo and is used to obtain information and perform operations at the silo level.
old-location: enstor\ienhancedstoragesilo.htm
tech.root: enstor
ms.assetid: 041e66d2-f772-407d-85f7-71f226c7ec4b
ms.date: 12/05/2018
ms.keywords: IEnhancedStorageSilo, IEnhancedStorageSilo interface [Enhanced Storage], IEnhancedStorageSilo interface [Enhanced Storage],described, ehstorapi/IEnhancedStorageSilo, enstor.ienhancedstoragesilo
f1_keywords:
- ehstorapi/IEnhancedStorageSilo
dev_langs:
- c++
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
- COM
api_location:
- EhStorAPI.h
api_name:
- IEnhancedStorageSilo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnhancedStorageSilo interface


## -description


The <b>IEnhancedStorageSilo</b> interface is the point of access for an IEEE 1667 silo and is used to obtain information and perform operations at the silo level.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnhancedStorageSilo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnhancedStorageSilo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnhancedStorageSilo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesilo-getactions">GetActions</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all actions available to the silo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesilo-getdevicepath">GetDevicePath</a>
</td>
<td align="left" width="63%">
Returns the path to the silo device node. The supplied string is suitable for passing to Windows System APIs such as <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea">SetupDiOpenDeviceInterface</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesilo-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Returns the general information associated with the silo object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesilo-getportabledevice">GetPortableDevice</a>
</td>
<td align="left" width="63%">
Obtains an <a href="https://go.microsoft.com/fwlink/p/?linkid=134792">IPortableDevice</a> pointer used to issue  commands to the corresponding Enhanced Storage silo driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesilo-sendcommand">SendCommand</a>
</td>
<td align="left" width="63%">
Sends a raw silo command to the silo object. This method is used to communicate with a silo which is not represented by a driver. 

</td>
</tr>
</table> 

