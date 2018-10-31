---
UID: NF:shlwapi.QISearch
title: QISearch function
author: windows-sdk-content
description: A table-driven implementation of the IUnknown::QueryInterface method.
old-location: shell\QISearch.htm
tech.root: shell
ms.assetid: 8429778b-bc9c-43f6-8d75-0fb78e36e790
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: QISearch, QISearch function [Windows Shell], _win32_QISearch, shell.QISearch, shlwapi/QISearch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - QISearch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QISearch function


## -description


A table-driven implementation of the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method.


## -parameters




### -param that [in]

Type: <b>void*</b>

A pointer to the base of a COM object.


### -param pqit [in]

Type: <b>LPCQITAB</b>

An array of <a href="https://msdn.microsoft.com/3a055773-6e53-45e1-8936-011a8b2b8b16">QITAB</a> structures. The last structure in the array must have its <b>piid</b> member set to <b>NULL</b> and its <b>dwOffset</b> member set to 0.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the requested interface was found in the table or if the requested interface was IUnknown. Returns E_NOINTERFACE if the requested interface was not found.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows Vista, <b>QISearch</b> was not exported by name or declared in a public header file. To use it in those cases, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 219 from Shlwapi.dll to obtain a function pointer. Under Windows Vista, <b>QISearch</b> is included in Shlwapi.h and this is not necessary.</div>
<div> </div>
If the requested interface is IUnknown, then <b>QISearch</b> uses the first entry of the specified array of <a href="https://msdn.microsoft.com/3a055773-6e53-45e1-8936-011a8b2b8b16">QITAB</a> structures. Otherwise, <b>QISearch</b> searches the table until it either finds a matching IID or reaches the end of the table.  If a matching IID is found, the function advances the associated interface pointer by the number of bytes specified by the <b>dwOffset</b> member of the interface's <b>QITAB</b> structure and reinterpreted as a COM pointer.  That pointer is assigned to the <b>QISearch</b> function's  <i>ppv</i> parameter. The method also calls IUnknown::AddRef to increment the interface's reference count.

If <b>QISearch</b> reaches the end of the table without finding the interface, it returns E_NOINTERFACE and sets <i>ppv</i> to <b>NULL</b>.

It is important to include all applicable interfaces in the table. For example, if the object implements a derived interface, you should also include the base interface in the table.

We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

<div class="alert"><b>Note</b>  Active Template Library (ATL) provides a significantly better version of a table-driven implementation of QueryInterface.</div>
<div> </div>

#### Examples

The following example illustrates how to use <b>QISearch</b> to implement QueryInterface.  It uses the offsetofclass macro from ATL to compute the offset from the base of the CSample object to a specified interface.

This object supports two interfaces aside from IUnknown, so there are two non-<b>NULL</b> entries in the <a href="https://msdn.microsoft.com/3a055773-6e53-45e1-8936-011a8b2b8b16">QITAB</a> table. The entry for each interface specifies a pointer to the associated IID (IID_IPersist or IID_IPersistFolder) and the offset of the interface pointer relative to the class's base pointer. The sample uses the <b>offsetofclass</b> macro from ATL to determine that offset.

<div class="alert"><b>Note</b>  Forgetting to include all base classes, including indirect ones, is a common error. Notice that there is an entry for the <a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a> interface. This interface is an indirect base class for CSample, inherited through <a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a>. </div>
<div> </div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
class CSample : public IPersistFolder
{
  public:
    CSample() { /* other construction goes here */ }
    
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
  
    // *** IPersist ***
    STDMETHODIMP GetClassID(CLSID *pClassID);
    
    // *** IPersistFolder ***
    STDMETHODIMP Initialize(LPCITEMIDLIST pidl);
  
  private:
  // private members go here
};

HRESULT CSample::QueryInterface(REFIID riid, void **ppv)
{
    static QITAB rgqit[] = 
    {   
        QITABENT(CSample, IPersist),
        QITABENT(CSample, IPersistFolder)
        { 0 },
    };

    return QISearch(this, rgqit, IID_PPV_ARGS(&amp;ppv));
}</pre>
</td>
</tr>
</table></span></div>


