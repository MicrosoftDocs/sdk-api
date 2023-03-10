---
UID: NS:propidlbase.tagPROPVARIANT
title: PROPVARIANT (propidlbase.h)
description: The PROPVARIANT structure is used in the ReadMultiple and WriteMultiple methods of IPropertyStorage to define the type tag and the value of a property in a property set. 
helpviewer_keywords: ["*LPPROPVARIANT","PROPVARIANT","PROPVARIANT structure [Structured Storage]","_stg_propvariant","propidlbase/PROPVARIANT","stg.propvariant","tagPROPVARIANT"]
old-location: stg\propvariant.htm
tech.root: Stg
ms.assetid: e86cc279-826d-4767-8d96-fc8280060ea1
ms.date: 08/02/2022
ms.keywords: '*LPPROPVARIANT, PROPVARIANT, PROPVARIANT structure [Structured Storage], _stg_propvariant, propidlbase/PROPVARIANT, stg.propvariant, tagPROPVARIANT'
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: PROPVARIANT, *LPPROPVARIANT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPROPVARIANT
 - propidlbase/tagPROPVARIANT
 - LPPROPVARIANT
 - propidlbase/LPPROPVARIANT
 - PROPVARIANT
 - propidlbase/PROPVARIANT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - propidlbase.h
api_name:
 - PROPVARIANT
---

# PROPVARIANT structure


## -description

The 
<b>PROPVARIANT</b> structure is used in the 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">ReadMultiple</a> and 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">WriteMultiple</a> methods of 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> to define the type tag and the value of a property in a property set.

The <b>PROPVARIANT</b> structure is also used by the <a href="/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)">GetValue</a> and <a href="/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)">SetValue</a> methods of <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>, which replaces <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> as the primary way to program item properties in Windows Vista. For more information, see <a href="/previous-versions//bb776861(v=vs.85)">Property Handlers</a>.

There are five members. The first member, the value-type tag, and the last member, the value of the property, are significant. The middle three members are reserved for future use.
<div class="alert"><b>Note</b>  The <b>bool</b> member in previous definitions of this structure has been renamed to <b>boolVal</b>, because some compilers now recognize <b>bool</b> as a keyword.</div><div> </div><div class="alert"><b>Note</b>  The 
<b>PROPVARIANT</b> structure, defined below, includes types that can be serialized in the version 1 property set serialization format. The version 1 format supports all types allowed in the version 0 format plus some additional types. The added types include "Version 1" in the comment field below. Use these types only if a version 1 property set is intended. For more information, see 
<a href="/windows/desktop/Stg/version-0-vs--version-1-property-set-serialization">Property Set Serialization</a>.</div><div> </div>The 
<b>PROPVARIANT</b> structure is defined as follows:

## -struct-fields

### -field tag_inner_PROPVARIANT

### -field tag_inner_PROPVARIANT.vt

### -field tag_inner_PROPVARIANT.wReserved1

### -field tag_inner_PROPVARIANT.wReserved2

### -field tag_inner_PROPVARIANT.wReserved3

### -field tag_inner_PROPVARIANT.cVal

### -field tag_inner_PROPVARIANT.bVal

### -field tag_inner_PROPVARIANT.iVal

### -field tag_inner_PROPVARIANT.uiVal

### -field tag_inner_PROPVARIANT.lVal

### -field tag_inner_PROPVARIANT.ulVal

### -field tag_inner_PROPVARIANT.intVal

### -field tag_inner_PROPVARIANT.uintVal

### -field tag_inner_PROPVARIANT.hVal

### -field tag_inner_PROPVARIANT.uhVal

### -field tag_inner_PROPVARIANT.fltVal

### -field tag_inner_PROPVARIANT.dblVal

### -field tag_inner_PROPVARIANT.boolVal

### -field tag_inner_PROPVARIANT.scode

### -field tag_inner_PROPVARIANT.cyVal

### -field tag_inner_PROPVARIANT.date

### -field tag_inner_PROPVARIANT.filetime

### -field tag_inner_PROPVARIANT.puuid

### -field tag_inner_PROPVARIANT.pclipdata

### -field tag_inner_PROPVARIANT.bstrVal

### -field tag_inner_PROPVARIANT.bstrblobVal

### -field tag_inner_PROPVARIANT.blob

### -field tag_inner_PROPVARIANT.pszVal

### -field tag_inner_PROPVARIANT.pwszVal

### -field tag_inner_PROPVARIANT.punkVal

### -field tag_inner_PROPVARIANT.pdispVal

### -field tag_inner_PROPVARIANT.pStream

### -field tag_inner_PROPVARIANT.pStorage

### -field tag_inner_PROPVARIANT.pVersionedStream

### -field tag_inner_PROPVARIANT.parray

### -field tag_inner_PROPVARIANT.cac

### -field tag_inner_PROPVARIANT.caub

### -field tag_inner_PROPVARIANT.cai

### -field tag_inner_PROPVARIANT.caui

### -field tag_inner_PROPVARIANT.cal

### -field tag_inner_PROPVARIANT.caul

### -field tag_inner_PROPVARIANT.cah

### -field tag_inner_PROPVARIANT.cauh

### -field tag_inner_PROPVARIANT.caflt

### -field tag_inner_PROPVARIANT.cadbl

### -field tag_inner_PROPVARIANT.cabool

### -field tag_inner_PROPVARIANT.cascode

### -field tag_inner_PROPVARIANT.cacy

### -field tag_inner_PROPVARIANT.cadate

### -field tag_inner_PROPVARIANT.cafiletime

### -field tag_inner_PROPVARIANT.cauuid

### -field tag_inner_PROPVARIANT.caclipdata

### -field tag_inner_PROPVARIANT.cabstr

### -field tag_inner_PROPVARIANT.cabstrblob

### -field tag_inner_PROPVARIANT.calpstr

### -field tag_inner_PROPVARIANT.calpwstr

### -field tag_inner_PROPVARIANT.capropvar

### -field tag_inner_PROPVARIANT.pcVal

### -field tag_inner_PROPVARIANT.pbVal

### -field tag_inner_PROPVARIANT.piVal

### -field tag_inner_PROPVARIANT.puiVal

### -field tag_inner_PROPVARIANT.plVal

### -field tag_inner_PROPVARIANT.pulVal

### -field tag_inner_PROPVARIANT.pintVal

### -field tag_inner_PROPVARIANT.puintVal

### -field tag_inner_PROPVARIANT.pfltVal

### -field tag_inner_PROPVARIANT.pdblVal

### -field tag_inner_PROPVARIANT.pboolVal

### -field tag_inner_PROPVARIANT.pdecVal

### -field tag_inner_PROPVARIANT.pscode

### -field tag_inner_PROPVARIANT.pcyVal

### -field tag_inner_PROPVARIANT.pdate

### -field tag_inner_PROPVARIANT.pbstrVal

### -field tag_inner_PROPVARIANT.ppunkVal

### -field tag_inner_PROPVARIANT.ppdispVal

### -field tag_inner_PROPVARIANT.pparray

### -field tag_inner_PROPVARIANT.pvarVal

### -field decVal

 




#### - bVal

<b>VT_UI1</b>


#### - blob

<b>VT_BLOB</b>, <b>VT_BLOBOBJECT</b>


#### - boolVal

<b>VT_BOOL</b>


#### - bstrVal

<b>VT_BSTR</b>


#### - bstrblobVal

<b>VT_BSTR_BLOB</b>


#### - cVal

<b>VT_I1</b>, Version 1


#### - cabool

<b>VT_VECTOR</b> | <b>VT_BOOL</b>


#### - cabstr

<b>VT_VECTOR</b> | <b>VT_BSTR</b>


#### - cabstrblob

<b>VT_VECTOR</b> | <b>VT_BSTR_BLOB</b>


#### - cac

<b>VT_VECTOR</b> | <b>VT_I1</b>, Version 1


#### - caclipdata

<b>VT_VECTOR</b> | <b>VT_CF</b>


#### - cacy

<b>VT_VECTOR</b> | <b>VT_CY</b>


#### - cadate

<b>VT_VECTOR</b> | <b>VT_DATE</b>


#### - cadbl

<b>VT_VECTOR</b> | <b>VT_R8</b>


#### - cafiletime

<b>VT_VECTOR</b> | <b>VT_FILETIME</b>


#### - caflt

<b>VT_VECTOR</b> | <b>VT_R4</b>


#### - cah

<b>VT_VECTOR</b> | <b>VT_I8</b>


#### - cai

<b>VT_VECTOR</b> | <b>VT_I2</b>


#### - cal

<b>VT_VECTOR</b> | <b>VT_I4</b>


#### - calpstr

<b>VT_VECTOR</b> | <b>VT_LPSTR</b>


#### - calpwstr

<b>VT_VECTOR</b> | <b>VT_LPWSTR</b>


#### - capropvar

<b>VT_VECTOR</b> | <b>VT_VARIANT</b>


#### - cascode

<b>VT_VECTOR</b> | <b>VT_ERROR</b>


#### - caub

<b>VT_VECTOR</b> | <b>VT_UI1</b>


#### - cauh

<b>VT_VECTOR</b> | <b>VT_UI8</b>


#### - caui

<b>VT_VECTOR</b> | <b>VT_UI2</b>


#### - caul

<b>VT_VECTOR</b> | <b>VT_UI4</b>


#### - cauuid

<b>VT_VECTOR</b> | <b>VT_CLSID</b>


#### - cyVal

<b>VT_CY</b>


#### - date

<b>VT_DATE</b>


#### - dblVal

<b>VT_R8</b>


#### - filetime

<b>VT_FILETIME</b>


#### - fltVal

<b>VT_R4</b>


#### - hVal

<b>VT_I8</b>


#### - iVal

<b>VT_I2</b>


#### - intVal

<b>VT_INT</b>, Version 1


#### - lVal

<b>VT_I4</b>


#### - pStorage

<b>VT_STORAGE</b>, <b>VT_STORED_OBJECT</b>


#### - pStream

<b>VT_STREAM</b>, <b>VT_STREAMED_OBJECT</b>


#### - pVersionedStream

<b>VT_VERSIONED_STREAM</b>


#### - parray

<b>VT_ARRAY</b> | <b>VT_*</b>, Version 1


#### - pbVal

<b>VT_BYREF</b> | <b>VT_UI1</b>, Version 1


#### - pboolVal

<b>VT_BYREF</b> | <b>VT_BOOL</b>, Version 1


#### - pbstrVal

<b>VT_BYREF</b> | <b>VT_BSTR</b>, Version 1


#### - pcVal

<b>VT_BYREF</b> | <b>VT_I1</b>, Version 1


#### - pclipdata

<b>VT_CF</b>


#### - pcyVal

<b>VT_BYREF</b> | <b>VT_CY</b>, Version 1


#### - pdate

<b>VT_BYREF</b> | <b>VT_DATE</b>, Version 1


#### - pdblVal

<b>VT_BYREF</b> | <b>VT_R8</b>, Version 1


#### - pdecVal

<b>VT_BYREF</b> | <b>VT_DECIMAL</b>, Version 1


#### - pdispVal

<b>VT_DISPATCH</b>


#### - pfltVal

<b>VT_BYREF</b> | <b>VT_R4</b>, Version 1


#### - piVal

<b>VT_BYREF</b> | <b>VT_I2</b>, Version 1


#### - pintVal

<b>VT_BYREF</b> | <b>VT_INT</b>, Version 1


#### - plVal

<b>VT_BYREF</b> | <b>VT_I4</b>, Version 1


#### - pparray

<b>VT_BYREF</b> | <b>VT_ARRAY</b>, Version 1


#### - ppdispVal

<b>VT_BYREF</b> | <b>VT_DISPATCH</b>, Version 1


#### - ppunkVal

<b>VT_BYREF</b> | <b>VT_UNKNOWN</b>, Version 1


#### - pscode

<b>VT_BYREF</b> | <b>VT_ERROR</b>, Version 1


#### - pszVal

<b>VT_LPSTR</b>


#### - puiVal

<b>VT_BYREF</b> | <b>VT_UI2</b>, Version 1


#### - puintVal

<b>VT_BYREF</b> | <b>VT_UINT</b>, Version 1


#### - pulVal

<b>VT_BYREF</b> | <b>VT_UI4</b>, Version 1


#### - punkVal

<b>VT_UNKNOWN</b>


#### - puuid

<b>VT_CLSID</b>


#### - pvarVal

<b>VT_BYREF</b> | <b>VT_VARIANT</b>, Version 1


#### - pwszVal

<b>VT_LPWSTR</b>


#### - scode

<b>VT_ERROR</b>


#### - uhVal

<b>VT_UI8</b>


#### - uiVal

<b>VT_UI2</b>


#### - uintVal

<b>VT_UINT</b>, Version 1


#### - ulVal

<b>VT_UI4</b>


#### - vt

Value type tag.


#### - wReserved1

Reserved for future use.


#### - wReserved2

Reserved for future use.


#### - wReserved3

Reserved for future use.

## -remarks

The 
<b>PROPVARIANT</b> structure can also hold a value of <b>VT_DECIMAL</b>:


``` syntax
    DECIMAL       decVal;        //VT_DECIMAL
```

However, the value of the <b>DECIMAL</b> structure requires special handling. The <b>DECIMAL</b> structure is the same size as an entire 
<b>PROPVARIANT</b> structure and does not fit into the union that holds all other types of values. Instead, the value of the <b>DECIMAL</b> structure occupies the entire 
<b>PROPVARIANT</b> structure, including the reserved fields and the <b>vt</b> member. However, the first member of the <b>DECIMAL</b> structure is not used and is equal in size to the <b>vt</b> member of the 
<b>PROPVARIANT</b> structure. Therefore, the 
<b>PROPVARIANT</b> structure declaration in the Propidl.h header file of Win32 defines the <b>decVal</b> member in such a way that it corresponds to the beginning of the 
<b>PROPVARIANT</b> structure. Therefore, to put the value of the <b>DECIMAL</b> structure into a 
<b>PROPVARIANT</b> structure, the value must be loaded into the <b>decVal</b> member and the <b>vt</b> member is set to <b>VT_DECIMAL</b>, just as for any other value.

<b>PROPVARIANT</b> is the fundamental data type by which property values are read and written through the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface.

The data type 
<b>PROPVARIANT</b> is related to the data type <b>VARIANT</b>, defined as part of Automation in OLE2. Several definitions are reused from Automation, as follows:


``` syntax
typedef struct  tagCY {
    unsigned long      Lo;
    long               Hi;
    } CY;
 
typedef struct  tagDEC {
    USHORT             wReserved;
    BYTE               scale;
    BYTE               sign;
    ULONG              Hi32;
    ULONGLONG          Lo64;
    } DECIMAL;
 
typedef struct  tagSAFEARRAYBOUND {
    ULONG              cElements;
    LONG               lLbound;
    } SAFEARRAYBOUND;
 
typedef struct  tagSAFEARRAY {
    USHORT             cDims;
    USHORT             fFeatures;
    ULONG              cbElements;
    ULONG              cLocks;
    PVOID              pvData;
    SAFEARRAYBOUND     rgsabound [ * ];
    } SAFEARRAY;
 
typedef CY             CURRENCY;
typedef short          VARIANT_BOOL;
typedef unsigned short VARTYPE;
typedef double         DATE;
typedef OLECHAR*       BSTR;
```

In addition, some types are unique to the 
<b>PROPVARIANT</b> structure:


``` syntax
typedef struct  tagCLIPDATA {
    // cbSize is the size of the buffer pointed to 
    // by pClipData, plus sizeof(ulClipFmt)
    ULONG              cbSize;
    long               ulClipFmt;
    BYTE*              pClipData;
    } CLIPDATA;
```

Among the unique 
<b>PROPVARIANT</b> types are several data types that define counted arrays of other data types. The data types of all counted arrays begin with the letters <b>CA</b>, for example <b>CAUB</b>, and have an <b>OR</b> operator <b>vt</b> value (the VarType of the element and an <b>OR</b> operator with <b>VT_VECTOR</b>). The counted array structure has the following form (where <i>name</i> is the specific name of the counted array).


``` syntax
#define TYPEDEF_CA(type, name) 
 
    typedef struct tag ## name {\
        ULONG cElems;\
        type *pElems;\
        } name
```

<table>
<tr>
<th>Propvariant type</th>
<th>Code</th>
<th>Propvariant member</th>
<th>Value representation</th>
</tr>
<tr>
<td><b>VT_EMPTY</b></td>
<td>0</td>
<td>None</td>
<td>A property with a type indicator of <b>VT_EMPTY</b> has no data associated with it; that is, the size of the value is zero.</td>
</tr>
<tr>
<td><b>VT_NULL</b></td>
<td>1</td>
<td>None</td>
<td>This is like a pointer to <b>NULL</b>.</td>
</tr>
<tr>
<td><b>VT_I1</b></td>
<td>16</td>
<td><b>cVal</b></td>
<td>1-byte signed integer.</td>
</tr>
<tr>
<td><b>VT_UI1</b></td>
<td>17</td>
<td><b>bVal</b></td>
<td>1-byte unsigned integer.</td>
</tr>
<tr>
<td><b>VT_I2</b></td>
<td>2</td>
<td><b>iVal</b></td>
<td>Two bytes representing a 2-byte signed integer value.</td>
</tr>
<tr>
<td><b>VT_UI2</b></td>
<td>18</td>
<td><b>uiVal</b></td>
<td>2-byte unsigned integer.</td>
</tr>
<tr>
<td><b>VT_I4</b></td>
<td>3</td>
<td><b>lVal</b></td>
<td>4-byte signed integer value.</td>
</tr>
<tr>
<td><b>VT_UI4</b></td>
<td>19</td>
<td><b>ulVal</b></td>
<td>4-byte unsigned integer.</td>
</tr>
<tr>
<td><b>VT_INT</b></td>
<td>22</td>
<td><b>intVal</b></td>
<td>4-byte signed integer value (equivalent to <b>VT_I4</b>).</td>
</tr>
<tr>
<td><b>VT_UINT</b></td>
<td>23</td>
<td><b>uintVal</b></td>
<td>4-byte unsigned integer (equivalent to <b>VT_UI4</b>).</td>
</tr>
<tr>
<td><b>VT_I8</b></td>
<td>20</td>
<td><b>hVal</b></td>
<td>8-byte signed integer.</td>
</tr>
<tr>
<td><b>VT_UI8</b></td>
<td>21</td>
<td><b>uhVal</b></td>
<td>8-byte unsigned integer.</td>
</tr>
<tr>
<td><b>VT_R4</b></td>
<td>4</td>
<td><b>fltVal</b></td>
<td>32-bit IEEE floating point value.</td>
</tr>
<tr>
<td><b>VT_R8</b></td>
<td>5</td>
<td><b>dblVal</b></td>
<td>64-bit IEEE floating point value.</td>
</tr>
<tr>
<td><b>VT_BOOL</b></td>
<td>11</td>
<td><b>boolVal</b> (<b>bool</b> in earlier designs)</td>
<td>Boolean value, a <b>WORD</b> that contains 0 (<b>FALSE</b>) or -1 (<b>TRUE</b>).</td>
</tr>
<tr>
<td><b>VT_ERROR</b></td>
<td>10</td>
<td><b>scode</b></td>
<td>A <b>DWORD</b> that contains a status code.</td>
</tr>
<tr>
<td><b>VT_CY</b></td>
<td>6</td>
<td><b>cyVal</b></td>
<td>8-byte two's complement integer (scaled by 10,000). This type is commonly used for currency amounts.</td>
</tr>
<tr>
<td><b>VT_DATE</b></td>
<td>7</td>
<td><b>date</b></td>
<td>A 64-bit floating point number representing the number of days (not seconds) since December 31, 1899. For example, January 1, 1900, is 2.0, January 2, 1900, is 3.0, and so on). This is stored in the same representation as <b>VT_R8</b>.</td>
</tr>
<tr>
<td><b>VT_FILETIME</b></td>
<td>64</td>
<td><b>filetime</b></td>
<td>64-bit <b>FILETIME</b> structure as defined by Win32. It is recommended that all times be stored in Universal Coordinate Time (UTC).</td>
</tr>
<tr>
<td><b>VT_CLSID</b></td>
<td>72</td>
<td><b>puuid</b></td>
<td>Pointer to a class identifier (CLSID) (or other globally unique identifier (GUID)).</td>
</tr>
<tr>
<td><b>VT_CF</b></td>
<td>71</td>
<td><b>pclipdata</b></td>
<td>Pointer to a <b>CLIPDATA</b> structure, described above.</td>
</tr>
<tr>
<td><b>VT_BSTR</b></td>
<td>8</td>
<td><b>bstrVal</b></td>
<td>Pointer to a null-terminated Unicode string. The string is immediately preceded by a <b>DWORD</b> representing the byte count, but <b>bstrVal</b> points past this <b>DWORD</b> to the first character of the string. <b>BSTR</b>s must be allocated and freed using the Automation <b>SysAllocString</b> and <b>SysFreeString</b> calls.</td>
</tr>
<tr>
<td><b>VT_BSTR_BLOB</b></td>
<td>0xfff</td>
<td><b>bstrblobVal</b></td>
<td>For system use only.</td>
</tr>
<tr>
<td><b>VT_BLOB</b></td>
<td>65</td>
<td><b>blob</b></td>
<td><b>DWORD</b> count of bytes, followed by that many bytes of data. The byte count does not include the four bytes for the length of the count itself; an empty <b>blob</b> member would have a count of zero, followed by zero bytes. This is similar to the value <b>VT_BSTR</b>, but does not guarantee a null byte at the end of the data.</td>
</tr>
<tr>
<td><b>VT_BLOBOBJECT</b></td>
<td>70</td>
<td><b>blob</b></td>
<td>A <b>blob</b> member that contains a serialized object in the same representation that would appear in <b>VT_STREAMED_OBJECT</b>. That is, a <b>DWORD</b> byte count (where the byte count does not include the size of itself) which is in the format of a class identifier followed by initialization data for that class. 


The only significant difference between <b>VT_BLOB_OBJECT</b> and <b>VT_STREAMED_OBJECT</b> is that the former does not have the system-level storage overhead that the latter would have, and is therefore more suitable for scenarios involving numbers of small objects.

</td>
</tr>
<tr>
<td><b>VT_LPSTR</b></td>
<td>30</td>
<td><b>pszVal</b></td>
<td>A pointer to a null-terminated ANSI string in the system default code page.</td>
</tr>
<tr>
<td><b>VT_LPWSTR</b></td>
<td>31</td>
<td><b>pwszVal</b></td>
<td>A pointer to a null-terminated Unicode string in the user default locale.</td>
</tr>
<tr>
<td><b>VT_UNKNOWN</b></td>
<td>13</td>
<td><b>punkVal</b></td>
<td>New.</td>
</tr>
<tr>
<td><b>VT_DISPATCH</b></td>
<td>9</td>
<td><b>pdispVal</b></td>
<td>New.</td>
</tr>
<tr>
<td><b>VT_STREAM</b></td>
<td>66</td>
<td><b>pStream</b></td>
<td>A pointer to an 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface that represents a stream which is a sibling to the "Contents" stream.</td>
</tr>
<tr>
<td><b>VT_STREAMED_OBJECT</b></td>
<td>68</td>
<td><b>pStream</b></td>
<td>As in <b>VT_STREAM</b>, but indicates that the stream contains a serialized object, which is a CLSID followed by initialization data for the class. The stream is a sibling to the "Contents" stream that contains the property set.</td>
</tr>
<tr>
<td><b>VT_STORAGE</b></td>
<td>67</td>
<td><b>pStorage</b></td>
<td>A pointer to an 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface, representing a storage object that is a sibling to the "Contents" stream.</td>
</tr>
<tr>
<td><b>VT_STORED_OBJECT</b></td>
<td>69</td>
<td><b>pStorage</b></td>
<td>As in <b>VT_STORAGE</b>, but indicates that the designated 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> contains a loadable object.</td>
</tr>
<tr>
<td><b>VT_VERSIONED_STREAM</b></td>
<td>73</td>
<td><b>pVersionedStream</b></td>
<td>A stream with a GUID version.</td>
</tr>
<tr>
<td><b>VT_DECIMAL</b></td>
<td>14</td>
<td><b>decVal</b></td>
<td>A <b>DECIMAL</b> structure.</td>
</tr>
<tr>
<td><b>VT_VECTOR</b></td>
<td>0x1000</td>
<td><b>ca*</b></td>
<td>If the type indicator is combined with <b>VT_VECTOR</b> by using an <b>OR</b> operator, the value is one of the counted array values. This creates a <b>DWORD</b> count of elements, followed by a pointer to the specified repetitions of the value. 


For example, a type indicator of <b>VT_LPSTR</b>|<b>VT_VECTOR</b> has a <b>DWORD</b> element count, followed by a pointer to an array of <b>LPSTR</b> elements.

<b>VT_VECTOR</b> can be combined by an <b>OR</b> operator with the following types: <b>VT_I1</b>, <b>VT_UI1</b>, <b>VT_I2</b>, <b>VT_UI2</b>, <b>VT_BOOL</b>, <b>VT_I4</b>, <b>VT_UI4</b>, <b>VT_R4</b>, <b>VT_R8</b>, <b>VT_ERROR</b>, <b>VT_I8</b>, <b>VT_UI8</b>, <b>VT_CY</b>, <b>VT_DATE</b>, <b>VT_FILETIME</b>, <b>VT_CLSID</b>, <b>VT_CF</b>, <b>VT_BSTR</b>, <b>VT_LPSTR</b>, <b>VT_LPWSTR</b>, and <b>VT_VARIANT</b>.  <b>VT_VECTOR</b> can also be combined by an <b>OR</b> operation with  <b>VT_BSTR_BLOB</b>, however it is for system use only.

</td>
</tr>
<tr>
<td><b>VT_ARRAY</b></td>
<td>0x2000</td>
<td><b>Parray</b></td>
<td>If the type indicator is combined with <b>VT_ARRAY</b> by an <b>OR</b> operator, the value is a pointer to a SAFEARRAY. <b>VT_ARRAY</b> can use the <b>OR</b> with the following data types: <b>VT_I1</b>, <b>VT_UI1</b>, <b>VT_I2</b>, <b>VT_UI2</b>, <b>VT_I4</b>, <b>VT_UI4</b>, <b>VT_INT</b>, <b>VT_UINT</b>, <b>VT_R4</b>, <b>VT_R8</b>, <b>VT_BOOL</b>, <b>VT_DECIMAL</b>, <b>VT_ERROR</b>, <b>VT_CY</b>, <b>VT_DATE</b>, <b>VT_BSTR</b>, <b>VT_DISPATCH</b>, <b>VT_UNKNOWN</b>, and <b>VT_VARIANT</b>. <b>VT_ARRAY</b> cannot use <b>OR</b> with <b>VT_VECTOR</b>.</td>
</tr>
<tr>
<td><b>VT_BYREF</b></td>
<td>0x4000</td>
<td><b>p*</b></td>
<td>If the type indicator is combined with <b>VT_BYREF</b> by an <b>OR</b> operator, the value is a reference. Reference types are interpreted as a reference to data, similar to the reference type in C++ (for example, "int&amp;"). 


VT_BYREF can use <b>OR</b> with the following types: <b>VT_I1</b>, <b>VT_UI1</b>, <b>VT_I2</b>, <b>VT_UI2</b>, <b>VT_I4</b>, <b>VT_UI4</b>, <b>VT_INT</b>, <b>VT_UINT</b>, <b>VT_R4</b>, <b>VT_R8</b>, <b>VT_BOOL</b>, <b>VT_DECIMAL</b>, <b>VT_ERROR</b>, <b>VT_CY</b>, <b>VT_DATE</b>, <b>VT_BSTR</b>, <b>VT_UNKNOWN</b>, <b>VT_DISPATCH</b>, <b>VT_ARRAY</b>, and <b>VT_VARIANT</b>.

</td>
</tr>
<tr>
<td><b>VT_VARIANT</b></td>
<td>12</td>
<td><b>capropvar</b></td>
<td>A <b>DWORD</b> type indicator followed by the corresponding value. <b>VT_VARIANT</b> can be used only with <b>VT_VECTOR</b> or <b>VT_BYREF</b>.</td>
</tr>
<tr>
<td><b>VT_TYPEMASK</b></td>
<td>0xFFF</td>
<td> </td>
<td>Used as a mask for <b>VT_VECTOR</b> and other modifiers to extract the raw VT value.</td>
</tr>
</table>
 

Clipboard format identifiers, stored with the tag VT_CF, use one of five representations, identified in the <b>ulClipFmt</b> member of the <b>CLIPDATA</b> structure using the <b>pClipData</b> pointer to the particular data type.

<table>
<tr>
<th><b>ulClipFmt</b> value</th>
<th><b>pClipData</b> value</th>
</tr>
<tr>
<td>-1L</td>
<td>A <b>DWORD</b> that contains a built-in Windows clipboard format value.</td>
</tr>
<tr>
<td>-2L</td>
<td>A <b>DWORD</b> that contains a Macintosh clipboard format value.</td>
</tr>
<tr>
<td>-3L</td>
<td>A GUID that contains a format identifier (FMTID). This is rarely used.</td>
</tr>
<tr>
<td>any positive value</td>
<td>A null-terminated string that contains a Windows clipboard format name, one suitable for passing to the <b>RegisterClipboardFormat</b> function. This function registers a new clipboard format. If a registered format with the specified name already exists, a new format is not registered and the return value identifies the existing format. This enables more than one application to copy and paste data using the same registered clipboard format. The format name comparison is case insensitive and is identified by values in the range from 0xC000 through 0xFFFF. The code page used for characters in the string is according to the code-page indicator. The "positive value" here is the string length, including the null byte at the end. When register clipboard formats are placed on or retrieved from the clipboard, they must be in the form of an <b>HGLOBAL</b> data-type value, which provides the handle to the object.</td>
</tr>
<tr>
<td>0L</td>
<td>No data (rarely used).</td>
</tr>
</table>
 

If the value of the <b>ulClipFmt</b> member is -1, the data is in the form of a built-in Windows format. In this case, the first <b>DWORD</b> of the buffer pointed to by <b>pClipData</b> is the clipboard format identifier, for example CF_METAFILEPICT. In the case of CF_METAFILEPCT, what follows is a variation on the <b>METAFILEPICT</b> structure (it uses <b>WORD</b>, rather than <b>DWORD</b> data types). That is, this data is in the following form:


``` syntax
struct PACKEDMETA
{
    WORD mm;
    WORD xExt;
    WORD yExt
    WORD reserved;
};
```

After the <b>METAFILEPICT</b> structure is the metafile data, suitable to be passed to the <b>SetMetaFileBitsEx</b> function. This function creates a memory-based, Windows-format metafile from the supplied data. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the <b>SetEnhMetaFileBits</b> function. This function retrieves the contents of the specified enhanced-format metafile and copies them into a buffer. If the function succeeds and the buffer pointer is <b>NULL</b>, the return value is the size of the enhanced metafile in bytes. If the function succeeds and the buffer pointer is a valid pointer, the return value is the number of bytes copied to the buffer. If the function fails, the return value is zero.

When register clipboard formats are placed on or retrieved from the clipboard, they must be in the form of an <b>HGLOBAL</b> value.
