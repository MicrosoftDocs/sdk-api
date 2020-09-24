---
UID: NF:mmc.IConsoleNameSpace2.AddExtension
title: IConsoleNameSpace2::AddExtension (mmc.h)
description: The IConsoleNameSpace2::AddExtension method enables the snap-in to add an extension snap-in that dynamically extends the namespace of a selected item.
helpviewer_keywords: ["AddExtension","AddExtension method [MMC]","AddExtension method [MMC]","IConsoleNameSpace2 interface","IConsoleNameSpace2 interface [MMC]","AddExtension method","IConsoleNameSpace2.AddExtension","IConsoleNameSpace2::AddExtension","_slate_iconsolenamespace2_addextension","mmc.iconsolenamespace2_addextension","mmc/IConsoleNameSpace2::AddExtension"]
old-location: mmc\iconsolenamespace2_addextension.htm
tech.root: mmc
ms.assetid: 6057b8dd-d794-43a3-998b-689aafa28b9d
ms.date: 12/05/2018
ms.keywords: AddExtension, AddExtension method [MMC], AddExtension method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace2 interface [MMC],AddExtension method, IConsoleNameSpace2.AddExtension, IConsoleNameSpace2::AddExtension, _slate_iconsolenamespace2_addextension, mmc.iconsolenamespace2_addextension, mmc/IConsoleNameSpace2::AddExtension
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsoleNameSpace2::AddExtension
 - mmc/IConsoleNameSpace2::AddExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleNameSpace2.AddExtension
---

# IConsoleNameSpace2::AddExtension


## -description

The <b>IConsoleNameSpace2::AddExtension</b> method enables the snap-in to add an extension snap-in that dynamically extends the namespace of a selected item.

## -parameters

### -param hItem [in]

A handle to the item to extend with the snap-in specified by <i>lpClsid</i>.

### -param lpClsid [in]

A pointer to the <b>CLSID</b> of the snap-in that will extend the namespace of the item specified by <i>hItem</i>.

## -returns

This method can return one of these values.

## -remarks

When a snap-in calls the 
AddExtension method, the namespace extension specified by lpClsid extends only the specific instance of the item specified by hItem. Other items of that type are not affected: Calling 
AddExtension is not the same as using the snap-in manager to add an extension to a snap-in. By using the snap-in manager to add an extension to a snap-in, the extension is added to all instances of snap-ins of that type.

In addition, the 
AddExtension method only works for items that are directly owned by the snap-in making the 
AddExtension call. For example, if a snap-in has a namespace extension that adds an item to its namespace, the snap-in cannot call 
AddExtension for the item provided by the namespace extension because the snap-in does not own that item.

A common place to add dynamic namespace extensions is in the <a href="/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a> notification handler of the snap-in's 
IComponentData object.

<div class="alert"><b>Note</b>  The extension snap-in must be a namespace extension. In addition, the MMC registry entries for the snap-in to be extended, as well as the extension snap-in, must be set correctly.</div>
<div> </div>
To dynamically add other types of extensions (such as context menus, toolbars, property sheets, or taskpads), the snap-in must add the new clipboard format CCF_MMC_DYNAMIC_EXTENSIONS to the data object for the items you want to extend. The 
<a href="/previous-versions/windows/desktop/mmc/ccf-mmc-dynamic-extensions">CCF_MMC_DYNAMIC_EXTENSIONS</a> format uses the 
<a href="/windows/desktop/api/mmc/ns-mmc-smmcobjecttypes">SMMCDynamicExtensions</a> structure. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/dynamic-non-namespace-extensions">Dynamic Non-Namespace Extensions</a>.

If an extension snap-in is intended to be used as a dynamic extension only, that extension snap-in should not be listed in the Available Extensions list box when the primary snap-in is selected in the Snap-in that can be extended box on the snap-in manager's extensions page. To hide an extension in the snap-in manager, add the key "Dynamic Extensions" to the key that represents the node type of the item you want to extend. Then put the CLSIDs of the snap-ins that should only dynamically extend the node type as values under the new key.


#### Examples

The following code example adds the extension snap-in specified by <b>CLSID_Extension</b>:


```cpp
IConsoleNameSpace2* pExtensions = NULL;
HRESULT hr = m_pConsole->QueryInterface(IID_IConsoleNameSpace2, reinterpret_cast<void**>(&pExtensions));
 
if (SUCCEEDED(hr))
{
    hr = pExtensions->AddExtension(m_pStaticRoot, const_cast<CLSID*>(&CLSID_Extension));
    ASSERT(hr == S_OK);
    pExtensions->Release();
}
```

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>