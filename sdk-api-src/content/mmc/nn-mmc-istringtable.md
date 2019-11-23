---
UID: NN:mmc.IStringTable
title: IStringTable (mmc.h)

description: The IStringTable interface is introduced in MMC 1.1.
old-location: mmc\istringtable.htm
tech.root: mmc
ms.assetid: 3b4cfc92-4f50-4b62-bb2c-77c8e0e003da

ms.date: 12/05/2018
ms.keywords: IStringTable, IStringTable interface [MMC], IStringTable interface [MMC],described, _slate_istringtable, mmc.istringtable, mmc/IStringTable
ms.topic: interface
f1_keywords: 
 - "mmc/IStringTable"
dev_langs:
 - c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IStringTable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStringTable interface


## -description


The 
<b>IStringTable</b> interface is introduced in MMC 1.1.

The 
<b>IStringTable</b> interface provides a way to store string data with the snap-in. A string table is created in the console file as required for each snap-in by MMC.

The 
<b>IStringTable</b> interface allows strings to be saved in the console file. Be aware that this interface is designed to work with specialized localization tools. Snap-ins without access to these localization tools will not benefit from using this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringTable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStringTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStringTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-addstring">AddString</a>
</td>
<td align="left" width="63%">
Adds a string to the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-deleteallstrings">DeleteAllStrings</a>
</td>
<td align="left" width="63%">
Removes all string from the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-deletestring">DeleteString</a>
</td>
<td align="left" width="63%">
Removes a string from the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-enumerate">Enumerate</a>
</td>
<td align="left" width="63%">
Returns an enumerator into a snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-findstring">FindString</a>
</td>
<td align="left" width="63%">
Finds a string in the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-getstring">GetString</a>
</td>
<td align="left" width="63%">
Retrieves a string from the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-getstringlength">GetStringLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of a string from the snap-in string table.

</td>
</tr>
</table> 

