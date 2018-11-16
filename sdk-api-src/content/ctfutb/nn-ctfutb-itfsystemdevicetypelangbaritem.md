---
UID: NN:ctfutb.ITfSystemDeviceTypeLangBarItem
title: ITfSystemDeviceTypeLangBarItem
author: windows-sdk-content
description: The ITfSystemDeviceTypeLangBarItem interface is implemented by a system language bar item and used by an application or text service to control how the system item displays its icon.
old-location: tsf\itfsystemdevicetypelangbaritem.htm
tech.root: TSF
ms.assetid: 0dc32f10-eecd-4203-992c-80eb0f991615
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITfSystemDeviceTypeLangBarItem, ITfSystemDeviceTypeLangBarItem interface [Text Services Framework], ITfSystemDeviceTypeLangBarItem interface [Text Services Framework],described, _tsf_itfsystemdevicetypelangbaritem_ref, ctfutb/ITfSystemDeviceTypeLangBarItem, tsf.itfsystemdevicetypelangbaritem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSystemDeviceTypeLangBarItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfSystemDeviceTypeLangBarItem interface


## -description


The <b>ITfSystemDeviceTypeLangBarItem</b> interface is implemented by a system language bar item and used by an application or text service to control how the system item displays its icon. The application or text service obtains an instance of this interface by calling QueryInterface on the <a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a> object with IID_ITfSystemDeviceTypeLangBarItem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSystemDeviceTypeLangBarItem</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfSystemDeviceTypeLangBarItem</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ITfSystemDeviceTypeLangBarItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628954(v=VS.85).aspx">GetIconMode</a>
</td>
<td align="left" width="63%">
Obtains the current icon display mode for a system language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628955(v=VS.85).aspx">SetIconMode</a>
</td>
<td align="left" width="63%">
Modifies the type of icon displayed for a system language bar item.

</td>
</tr>
</table> 


## -remarks



Support for this interface is optional and must not be assumed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

