---
UID: NF:uiribbon.IUISimplePropertySet.GetValue
title: IUISimplePropertySet::GetValue
author: windows-sdk-content
description: Retrieves the value identified by a property key.
old-location: windowsribbon\windowsribbon_iuisimplepropertyset_getvalue.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuisimplepropertyset\getvalue.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetValue, GetValue method [Windows Ribbon], GetValue method [Windows Ribbon],IUISimplePropertySet interface, IUISimplePropertySet interface [Windows Ribbon],GetValue method, IUISimplePropertySet.GetValue, IUISimplePropertySet::GetValue, scenicintent_IUISimplePropertySet_GetValue, uiribbon/IUISimplePropertySet::GetValue, windowsribbon.windowsribbon_iuisimplepropertyset_getvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUISimplePropertySet.GetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUISimplePropertySet::GetValue


## -description


Retrieves the value identified by a property key.
		


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="https://msdn.microsoft.com/en-us/library/Dd371196(v=VS.85).aspx">Property Key</a> of interest.
				


### -param value [out]

Type: <b>PROPVARIANT*</b>

When this method returns, contains a pointer to the value for 
					<i>key</i>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




#### Examples

The following example demonstrates a custom implementation of  <a href="https://msdn.microsoft.com/en-us/library/Dd371358(v=VS.85).aspx">IUISimplePropertySet</a> for both item and Command galleries.

The CItemProperties class in this example is derived from <a href="https://msdn.microsoft.com/en-us/library/Dd371358(v=VS.85).aspx">IUISimplePropertySet</a> and, in addition to the required method <b>IUISimplePropertySet::GetValue</b>, implements a set of helper functions for initialization and index tracking.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions added. 
//

class CItemProperties
  : public CComObjectRootEx&lt;CComMultiThreadModel&gt;
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
      if(key == UI_PKEY_CommandId &amp;&amp; _isCommandGallery)
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
                 MAKEINTRESOURCE(IDB_GALLERYITEM), &amp;_spimgItem);
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
  CComPtr&lt;IUIImage&gt; _spimgItem;	
};</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371358(v=VS.85).aspx">IUISimplePropertySet</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371196(v=VS.85).aspx">Property Keys</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

