---
UID: NF:uiribbon.IUISimplePropertySet.GetValue
title: IUISimplePropertySet::GetValue (uiribbon.h)
description: Retrieves the value identified by a property key.
helpviewer_keywords: ["GetValue","GetValue method [Windows Ribbon]","GetValue method [Windows Ribbon]","IUISimplePropertySet interface","IUISimplePropertySet interface [Windows Ribbon]","GetValue method","IUISimplePropertySet.GetValue","IUISimplePropertySet::GetValue","scenicintent_IUISimplePropertySet_GetValue","uiribbon/IUISimplePropertySet::GetValue","windowsribbon.windowsribbon_iuisimplepropertyset_getvalue"]
old-location: windowsribbon\windowsribbon_iuisimplepropertyset_getvalue.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuisimplepropertyset\getvalue.htm
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Windows Ribbon], GetValue method [Windows Ribbon],IUISimplePropertySet interface, IUISimplePropertySet interface [Windows Ribbon],GetValue method, IUISimplePropertySet.GetValue, IUISimplePropertySet::GetValue, scenicintent_IUISimplePropertySet_GetValue, uiribbon/IUISimplePropertySet::GetValue, windowsribbon.windowsribbon_iuisimplepropertyset_getvalue
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUISimplePropertySet::GetValue
 - uiribbon/IUISimplePropertySet::GetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUISimplePropertySet.GetValue
---

# IUISimplePropertySet::GetValue


## -description

Retrieves the value identified by a property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties">Property Key</a> of interest.

### -param value [out]

Type: <b>PROPVARIANT*</b>

When this method returns, contains a pointer to the value for 
					<i>key</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

#### Examples

The following example demonstrates a custom implementation of  <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset">IUISimplePropertySet</a> for both item and Command galleries.

The CItemProperties class in this example is derived from <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset">IUISimplePropertySet</a> and, in addition to the required method <b>IUISimplePropertySet::GetValue</b>, implements a set of helper functions for initialization and index tracking.


```cpp
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions added. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // A Command gallery.
		  // _isCommandGallery set on item initialization.
    if (_isCommandGallery)
    {			
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
			     // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }			
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(
                 UI_PKEY_Label, g_labels[_index], ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        if (NULL == _spimgItem)
        {
          hr = CreateUIImageFromBitmapResource(
                 MAKEINTRESOURCE(IDB_GALLERYITEM), &_spimgItem);
          if (FAILED(hr))
          {
            return hr;
          }
        }
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(
                 UI_PKEY_ItemImage, _spimgItem, ppropvar);
      }			
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;
  CComPtr<IUIImage> _spimgItem;	
};
```

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset">IUISimplePropertySet</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties">Property Keys</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>