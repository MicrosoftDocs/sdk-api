---
UID: TP:properties
ms.assetid: ad4462be-c0de-3130-918e-217804db0bf6
ms.author: windowssdkdev
ms.date: 06/09/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows Property System

## -description

Overview of the Windows Property System technology.

To develop Windows Property System, you need these headers:

 * [propidl.h](../propidl/index.md)
 * [propsys.h](../propsys/index.md)
 * [propvarutil.h](../propvarutil/index.md)
 * [shobjidl_core.h](../shobjidl_core/index.md)

For the programming guide, see [Windows Property System](/windows/desktop/properties).

## Functions

| Title   | Description   |
| ---- |:---- |
| [ClearPropVariantArray function](..\propvarutil\nf-propvarutil-clearpropvariantarray.md) | Frees the memory and references used by an array of PROPVARIANT structures stored in an array. |
| [ClearVariantArray function](..\propvarutil\nf-propvarutil-clearvariantarray.md) | Frees the memory and references used by an array of VARIANT structures stored in an array. |
| [FreePropVariantArray function](..\propidl\nf-propidl-freepropvariantarray.md) | Frees the memory and references used by an array of PROPVARIANT structures. |
| [InitPropVariantFromBoolean function](..\propvarutil\nf-propvarutil-initpropvariantfromboolean.md) | Initializes a given PROPVARIANT structure as a VT_BOOL using a specified Boolean value. |
| [InitPropVariantFromBooleanVector function](..\propvarutil\nf-propvarutil-initpropvariantfrombooleanvector.md) | Initializes a PROPVARIANT structure from a specified Boolean vector. |
| [InitPropVariantFromBuffer function](..\propvarutil\nf-propvarutil-initpropvariantfrombuffer.md) | Initializes a PROPVARIANT structure using the contents of a buffer. |
| [InitPropVariantFromCLSID function](..\propvarutil\nf-propvarutil-initpropvariantfromclsid.md) | Initializes a PROPVARIANT structure based on a class identifier (CLSID). |
| [InitPropVariantFromDouble function](..\propvarutil\nf-propvarutil-initpropvariantfromdouble.md) | Initializes a PROPVARIANT structure based on a specified double value. |
| [InitPropVariantFromDoubleVector function](..\propvarutil\nf-propvarutil-initpropvariantfromdoublevector.md) | Initializes a PROPVARIANT structure based on a specified vector of double values. |
| [InitPropVariantFromFileTime function](..\propvarutil\nf-propvarutil-initpropvariantfromfiletime.md) | Initializes a PROPVARIANT structure based on information stored in a FILETIME structure. |
| [InitPropVariantFromFileTimeVector function](..\propvarutil\nf-propvarutil-initpropvariantfromfiletimevector.md) | Initializes a PROPVARIANT structure from a specified vector of FILETIME values. |
| [InitPropVariantFromGUIDAsBuffer function](..\propvarutil\nf-propvarutil-initpropvariantfromguidasbuffer.md) | Initializes a PROPVARIANT structure based on a GUID. The structure is initialized as VT_VECTOR | VT_UI1. |
| [InitPropVariantFromGUIDAsString function](..\propvarutil\nf-propvarutil-initpropvariantfromguidasstring.md) | Initializes a PROPVARIANT structure based on a GUID. The structure is initialized as VT_LPWSTR. |
| [InitPropVariantFromInt16 function](..\propvarutil\nf-propvarutil-initpropvariantfromint16.md) | Initializes a PROPVARIANT structure based on a 16-bit integer value. |
| [InitPropVariantFromInt16Vector function](..\propvarutil\nf-propvarutil-initpropvariantfromint16vector.md) | Initializes a PROPVARIANT structure based on a specified vector of 16-bit integer values. |
| [InitPropVariantFromInt32 function](..\propvarutil\nf-propvarutil-initpropvariantfromint32.md) | Initializes a PROPVARIANT structure based on a 32-bit integer value. |
| [InitPropVariantFromInt32Vector function](..\propvarutil\nf-propvarutil-initpropvariantfromint32vector.md) | Initializes a PROPVARIANT structure based on a vector of 32-bit integer values. |
| [InitPropVariantFromInt64 function](..\propvarutil\nf-propvarutil-initpropvariantfromint64.md) | Initializes a PROPVARIANT structure based on a specified Int64 value. |
| [InitPropVariantFromInt64Vector function](..\propvarutil\nf-propvarutil-initpropvariantfromint64vector.md) | Initializes a PROPVARIANT structure based on a vector of Int64 values. |
| [InitPropVariantFromPropVariantVectorElem function](..\propvarutil\nf-propvarutil-initpropvariantfrompropvariantvectorelem.md) | Initializes a PROPVARIANT structure based on a specified PROPVARIANT vector element. |
| [InitPropVariantFromResource function](..\propvarutil\nf-propvarutil-initpropvariantfromresource.md) | Initializes a PROPVARIANT structure based on a string resource embedded in an executable file. |
| [InitPropVariantFromStrRet function](..\propvarutil\nf-propvarutil-initpropvariantfromstrret.md) | Initializes a PROPVARIANT structure based on a string stored in a STRRET structure. |
| [InitPropVariantFromString function](..\propvarutil\nf-propvarutil-initpropvariantfromstring.md) | Initializes a PROPVARIANT structure based on a specified string. |
| [InitPropVariantFromStringAsVector function](..\propvarutil\nf-propvarutil-initpropvariantfromstringasvector.md) | Initializes a PROPVARIANT structure from a specified string. The string is parsed as a semi-colon delimited list (for example |
| [InitPropVariantFromStringVector function](..\propvarutil\nf-propvarutil-initpropvariantfromstringvector.md) | Initializes a PROPVARIANT structure from a specified string vector. |
| [InitPropVariantFromUInt16 function](..\propvarutil\nf-propvarutil-initpropvariantfromuint16.md) | Initializes a PROPVARIANT structure based on a 16-bit unsigned integer value. |
| [InitPropVariantFromUInt16Vector function](..\propvarutil\nf-propvarutil-initpropvariantfromuint16vector.md) | Initializes a PROPVARIANT structure based on a vector of 16-bit unsigned integer values. |
| [InitPropVariantFromUInt32 function](..\propvarutil\nf-propvarutil-initpropvariantfromuint32.md) | Initializes a PROPVARIANT structure based on a 32-bit unsigned integer value. |
| [InitPropVariantFromUInt32Vector function](..\propvarutil\nf-propvarutil-initpropvariantfromuint32vector.md) | Initializes a PROPVARIANT structure based on a vector of 32-bit unsigned integer values. |
| [InitPropVariantFromUInt64 function](..\propvarutil\nf-propvarutil-initpropvariantfromuint64.md) | Initializes a PROPVARIANT structure with a 64-bit unsigned integer value. |
| [InitPropVariantFromUInt64Vector function](..\propvarutil\nf-propvarutil-initpropvariantfromuint64vector.md) | Initializes a PROPVARIANT structure based on a vector of 64-bit unsigned integers. |
| [InitPropVariantVectorFromPropVariant function](..\propvarutil\nf-propvarutil-initpropvariantvectorfrompropvariant.md) | Initializes a vector element in a PROPVARIANT structure with a value stored in another PROPVARIANT. |
| [InitVariantFromBoolean function](..\propvarutil\nf-propvarutil-initvariantfromboolean.md) | Initializes a VARIANT structure with a Boolean value. |
| [InitVariantFromBooleanArray function](..\propvarutil\nf-propvarutil-initvariantfrombooleanarray.md) | Initializes a VARIANT structure from an array of Boolean values. |
| [InitVariantFromBuffer function](..\propvarutil\nf-propvarutil-initvariantfrombuffer.md) | Initializes a VARIANT structure with the contents of a buffer. |
| [InitVariantFromDispatch function](..\propvarutil\nf-propvarutil-initvariantfromdispatch.md) | Initializes a VARIANT structure based on an instance of an IDispatch object. |
| [InitVariantFromDosDateTime function](..\propvarutil\nf-propvarutil-initvariantfromdosdatetime.md) | Initializes a VARIANT structure with a date and time given in the format used by Microsoft MS-DOS. The date and time values are converted to the format used to store date and time in a VARIANT. |
| [InitVariantFromDouble function](..\propvarutil\nf-propvarutil-initvariantfromdouble.md) | Initializes a VARIANT structure with a value of type DOUBLE. |
| [InitVariantFromDoubleArray function](..\propvarutil\nf-propvarutil-initvariantfromdoublearray.md) | Initializes a VARIANT structure with an array of values of type DOUBLE. |
| [InitVariantFromFileTime function](..\propvarutil\nf-propvarutil-initvariantfromfiletime.md) | Initializes a VARIANT structure with the contents of a FILETIME structure. |
| [InitVariantFromFileTimeArray function](..\propvarutil\nf-propvarutil-initvariantfromfiletimearray.md) | Initializes a VARIANT structure with an array of FILETIME structures. |
| [InitVariantFromGUIDAsBuffer function](..\propvarutil\nf-propvarutil-initvariantfromguidasbuffer.md) | Initializes a VARIANT structure based on a GUID. The structure is initialized as VT_ARRAY | VT_UI1. |
| [InitVariantFromGUIDAsString function](..\propvarutil\nf-propvarutil-initvariantfromguidasstring.md) | Initializes a VARIANT structure based on a GUID. The structure is initialized as a VT_BSTR type. |
| [InitVariantFromInt16 function](..\propvarutil\nf-propvarutil-initvariantfromint16.md) | Initializes a VARIANT structure with a 16-bit integer value. |
| [InitVariantFromInt16Array function](..\propvarutil\nf-propvarutil-initvariantfromint16array.md) | Initializes a VARIANT structure with an array of 16-bit integer values. |
| [InitVariantFromInt32 function](..\propvarutil\nf-propvarutil-initvariantfromint32.md) | Initializes a VARIANT structure with a 32-bit integer value. |
| [InitVariantFromInt32Array function](..\propvarutil\nf-propvarutil-initvariantfromint32array.md) | Initializes a VARIANT structure with an array of 32-bit integer values. |
| [InitVariantFromInt64 function](..\propvarutil\nf-propvarutil-initvariantfromint64.md) | Initializes a VARIANT structure with a 64-bit integer value. |
| [InitVariantFromInt64Array function](..\propvarutil\nf-propvarutil-initvariantfromint64array.md) | Initializes a VARIANT structure with an array of 64-bit integer values. |
| [InitVariantFromResource function](..\propvarutil\nf-propvarutil-initvariantfromresource.md) | Initializes a VARIANT structure based on a string resource imbedded in an executable file. |
| [InitVariantFromStrRet function](..\propvarutil\nf-propvarutil-initvariantfromstrret.md) | Initializes a VARIANT structure with a string stored in a STRRET structure. |
| [InitVariantFromString function](..\propvarutil\nf-propvarutil-initvariantfromstring.md) | Initializes a VARIANT structure with a string. |
| [InitVariantFromStringArray function](..\propvarutil\nf-propvarutil-initvariantfromstringarray.md) | Initializes a VARIANT structure with an array of strings. |
| [InitVariantFromUInt16 function](..\propvarutil\nf-propvarutil-initvariantfromuint16.md) | Initializes a VARIANT structure with an unsigned 16-bit integer value. |
| [InitVariantFromUInt16Array function](..\propvarutil\nf-propvarutil-initvariantfromuint16array.md) | Initializes a VARIANT structure with an array of unsigned 16-bit integer values. |
| [InitVariantFromUInt32 function](..\propvarutil\nf-propvarutil-initvariantfromuint32.md) | Initializes a VARIANT structure with an unsigned 32-bit integer value. |
| [InitVariantFromUInt32Array function](..\propvarutil\nf-propvarutil-initvariantfromuint32array.md) | Initializes a VARIANT structure with an array of unsigned 32-bit integer values. |
| [InitVariantFromUInt64 function](..\propvarutil\nf-propvarutil-initvariantfromuint64.md) | Initializes a VARIANT structure with an unsigned 64-bit integer value. |
| [InitVariantFromUInt64Array function](..\propvarutil\nf-propvarutil-initvariantfromuint64array.md) | Initializes a VARIANT structure with an array of unsigned 64-bit integer values. |
| [InitVariantFromVariantArrayElem function](..\propvarutil\nf-propvarutil-initvariantfromvariantarrayelem.md) | Initializes a VARIANT structure with a value stored in another VARIANT structure. |
| [IsPropVariantString function](..\propvarutil\nf-propvarutil-ispropvariantstring.md) | Specifies whether a specified PROPVARIANT structure is a string type. |
| [IsPropVariantVector function](..\propvarutil\nf-propvarutil-ispropvariantvector.md) | Specifies whether a PROPVARIANT structure has a vector type. |
| [IsVarTypeFloat function](..\propvarutil\nf-propvarutil-isvartypefloat.md) | Returns whether a VARTYPE is a float. |
| [IsVarTypeInteger function](..\propvarutil\nf-propvarutil-isvartypeinteger.md) | Returns whether a VARTYPE is an integer. |
| [IsVarTypeNumber function](..\propvarutil\nf-propvarutil-isvartypenumber.md) | Specifies whether VARTYPE is a number. |
| [IsVarTypeSignedInteger function](..\propvarutil\nf-propvarutil-isvartypesignedinteger.md) | Returns whether a VARTYPE is a signed integer. |
| [IsVarTypeUnsignedInteger function](..\propvarutil\nf-propvarutil-isvartypeunsignedinteger.md) | Returns whether a VARTYPE is an unsigned integer. |
| [IsVariantArray function](..\propvarutil\nf-propvarutil-isvariantarray.md) | Specifies whether a variant is an array. |
| [IsVariantString function](..\propvarutil\nf-propvarutil-isvariantstring.md) | Specifies whether a variant is a string. |
| [PSCoerceToCanonicalValue function](..\propsys\nf-propsys-pscoercetocanonicalvalue.md) | Converts the value of a property to the canonical value, according to the property description. |
| [PSCreateAdapterFromPropertyStore function](..\propsys\nf-propsys-pscreateadapterfrompropertystore.md) | Creates an adapter from an IPropertyStore. |
| [PSCreateDelayedMultiplexPropertyStore function](..\propsys\nf-propsys-pscreatedelayedmultiplexpropertystore.md) | Creates a read-only, delayed-binding property store that contains multiple property stores. |
| [PSCreateMemoryPropertyStore function](..\propsys\nf-propsys-pscreatememorypropertystore.md) | Creates an in-memory property store. |
| [PSCreateMultiplexPropertyStore function](..\propsys\nf-propsys-pscreatemultiplexpropertystore.md) | Creates a read-only property store that contains multiple property stores, each of which must support either IPropertyStore or IPropertySetStorage. |
| [PSCreatePropertyChangeArray function](..\propsys\nf-propsys-pscreatepropertychangearray.md) | Creates a container for a set of IPropertyChange objects. This container can be used with IFileOperation to apply a set of property changes to a set of files. |
| [PSCreatePropertyStoreFromObject function](..\propsys\nf-propsys-pscreatepropertystorefromobject.md) | Accepts the IUnknown interface of an object that supports IPropertyStore or IPropertySetStorage. If the object supports IPropertySetStorage, it is wrapped so that it supports IPropertyStore. |
| [PSCreatePropertyStoreFromPropertySetStorage function](..\propsys\nf-propsys-pscreatepropertystorefrompropertysetstorage.md) | Wraps an IPropertySetStorage interface in an IPropertyStore interface. |
| [PSCreateSimplePropertyChange function](..\propsys\nf-propsys-pscreatesimplepropertychange.md) | Creates a simple property change. |
| [PSEnumeratePropertyDescriptions function](..\propsys\nf-propsys-psenumeratepropertydescriptions.md) | A wrapper API that calls the schema subsystem's IPropertySystem |
| [PSFormatForDisplay function](..\propsys\nf-propsys-psformatfordisplay.md) | Gets a formatted, Unicode string representation of a property value stored in a PROPVARIANT structure. The caller is responsible for allocating the output buffer. |
| [PSFormatForDisplayAlloc function](..\propsys\nf-propsys-psformatfordisplayalloc.md) | Gets a formatted, Unicode string representation of a property value stored in a PROPVARIANT structure. This function allocates memory for the output string. |
| [PSFormatPropertyValue function](..\propsys\nf-propsys-psformatpropertyvalue.md) | Gets a formatted, Unicode string representation of a property value stored in a property store. This function allocates memory for the output string. |
| [PSGetImageReferenceForValue function](..\propsys\nf-propsys-psgetimagereferenceforvalue.md) | Gets an instance of a property description interface for a specified property. |
| [PSGetItemPropertyHandler function](..\propsys\nf-propsys-psgetitempropertyhandler.md) | Retrieves a property handler for a Shell item. |
| [PSGetItemPropertyHandlerWithCreateObject function](..\propsys\nf-propsys-psgetitempropertyhandlerwithcreateobject.md) | Retrieves a property handler for a Shell item. |
| [PSGetNameFromPropertyKey function](..\propsys\nf-propsys-psgetnamefrompropertykey.md) | Retrieves the canonical name of the property, given its PROPERTYKEY. |
| [PSGetNamedPropertyFromPropertyStorage function](..\propsys\nf-propsys-psgetnamedpropertyfrompropertystorage.md) | Gets a value from serialized property storage by property name. |
| [PSGetPropertyDescription function](..\propsys\nf-propsys-psgetpropertydescription.md) | Gets an instance of a property description interface for a property specified by a PROPERTYKEY structure. |
| [PSGetPropertyDescriptionByName function](..\propsys\nf-propsys-psgetpropertydescriptionbyname.md) | Gets an instance of a property description interface for a specified property name. |
| [PSGetPropertyDescriptionListFromString function](..\propsys\nf-propsys-psgetpropertydescriptionlistfromstring.md) | Gets an instance of a property description list interface for a specified property list. |
| [PSGetPropertyFromPropertyStorage function](..\propsys\nf-propsys-psgetpropertyfrompropertystorage.md) | Gets the value of a property as stored in serialized property storage. |
| [PSGetPropertyKeyFromName function](..\propsys\nf-propsys-psgetpropertykeyfromname.md) | Gets the property key for a canonical property name. |
| [PSGetPropertySystem function](..\propsys\nf-propsys-psgetpropertysystem.md) | Gets an instance of the subsystem object that implements IPropertySystem. |
| [PSGetPropertyValue function](..\propsys\nf-propsys-psgetpropertyvalue.md) | Gets a property value from a property store. |
| [PSLookupPropertyHandlerCLSID function](..\propsys\nf-propsys-pslookuppropertyhandlerclsid.md) | Gets the class identifier (CLSID) of a per-computer, registered file property handler. |
| [PSPropertyBag_Delete function](..\propsys\nf-propsys-pspropertybag_delete.md) | Deletes a property from a property bag. |
| [PSPropertyBag_ReadBOOL function](..\propsys\nf-propsys-pspropertybag_readbool.md) | Reads the BOOL data value of a property in a property bag. |
| [PSPropertyBag_ReadBSTR function](..\propsys\nf-propsys-pspropertybag_readbstr.md) | Reads a BSTR data value from a property in a property bag. |
| [PSPropertyBag_ReadDWORD function](..\propsys\nf-propsys-pspropertybag_readdword.md) | Reads a DWORD data value from property in a property bag. |
| [PSPropertyBag_ReadGUID function](..\propsys\nf-propsys-pspropertybag_readguid.md) | Reads the GUID data value from a property in a property bag. |
| [PSPropertyBag_ReadInt function](..\propsys\nf-propsys-pspropertybag_readint.md) | Reads an int data value from a property in a property bag. |
| [PSPropertyBag_ReadLONG function](..\propsys\nf-propsys-pspropertybag_readlong.md) | Reads a LONG data value from a property in a property bag. |
| [PSPropertyBag_ReadPOINTL function](..\propsys\nf-propsys-pspropertybag_readpointl.md) | Retrieves the property coordinates stored in a POINTL structure of a specified property bag. |
| [PSPropertyBag_ReadPOINTS function](..\propsys\nf-propsys-pspropertybag_readpoints.md) | Retrieves the property coordinates stored in a POINTS structure of a specified property bag. |
| [PSPropertyBag_ReadPropertyKey function](..\propsys\nf-propsys-pspropertybag_readpropertykey.md) | Reads the property key of a property in a specified property bag. |
| [PSPropertyBag_ReadRECTL function](..\propsys\nf-propsys-pspropertybag_readrectl.md) | Retrieves the coordinates of a rectangle stored in a property contained in a specified property bag. |
| [PSPropertyBag_ReadSHORT function](..\propsys\nf-propsys-pspropertybag_readshort.md) | Reads the SHORT data value of a property in a property bag. |
| [PSPropertyBag_ReadStr function](..\propsys\nf-propsys-pspropertybag_readstr.md) | Reads the string data value of a property in a property bag. |
| [PSPropertyBag_ReadStrAlloc function](..\propsys\nf-propsys-pspropertybag_readstralloc.md) | Reads a string data value from a property in a property bag and allocates memory for the string that is read. |
| [PSPropertyBag_ReadStream function](..\propsys\nf-propsys-pspropertybag_readstream.md) | Reads the data stream stored in a given property contained in a specified property bag. |
| [PSPropertyBag_ReadType function](..\propsys\nf-propsys-pspropertybag_readtype.md) | Reads the type of data value of a property that is stored in a property bag. |
| [PSPropertyBag_ReadULONGLONG function](..\propsys\nf-propsys-pspropertybag_readulonglong.md) | Reads a ULONGLONG data value from a property in a property bag. |
| [PSPropertyBag_ReadUnknown function](..\propsys\nf-propsys-pspropertybag_readunknown.md) | Reads a given property of an unknown data value in a property bag. |
| [PSPropertyBag_WriteBOOL function](..\propsys\nf-propsys-pspropertybag_writebool.md) | Sets the BOOL value of a property in a property bag. |
| [PSPropertyBag_WriteBSTR function](..\propsys\nf-propsys-pspropertybag_writebstr.md) | Sets the BSTR value of a property in a property bag. |
| [PSPropertyBag_WriteDWORD function](..\propsys\nf-propsys-pspropertybag_writedword.md) | Sets the DWORD value of a property in a property bag. |
| [PSPropertyBag_WriteGUID function](..\propsys\nf-propsys-pspropertybag_writeguid.md) | Sets the GUID value of a property in a property bag. |
| [PSPropertyBag_WriteInt function](..\propsys\nf-propsys-pspropertybag_writeint.md) | Sets the int value of a property in a property bag. |
| [PSPropertyBag_WriteLONG function](..\propsys\nf-propsys-pspropertybag_writelong.md) | Sets the LONG value of a property in a property bag. |
| [PSPropertyBag_WritePOINTL function](..\propsys\nf-propsys-pspropertybag_writepointl.md) | Stores the property coordinates in aPOINTL structure of a specified property bag. |
| [PSPropertyBag_WritePOINTS function](..\propsys\nf-propsys-pspropertybag_writepoints.md) | Stores the property coordinates in aPOINTS structure of a specified property bag. |
| [PSPropertyBag_WritePropertyKey function](..\propsys\nf-propsys-pspropertybag_writepropertykey.md) | Sets the property key value of a property in a property bag. |
| [PSPropertyBag_WriteRECTL function](..\propsys\nf-propsys-pspropertybag_writerectl.md) | Stores the coordinates of a rectangle in a property in a property bag. |
| [PSPropertyBag_WriteSHORT function](..\propsys\nf-propsys-pspropertybag_writeshort.md) | Sets the SHORT value of a property in a property bag. |
| [PSPropertyBag_WriteStr function](..\propsys\nf-propsys-pspropertybag_writestr.md) | Sets the string value of a property in a property bag. |
| [PSPropertyBag_WriteStream function](..\propsys\nf-propsys-pspropertybag_writestream.md) | Writes a data stream to a property in a property bag. |
| [PSPropertyBag_WriteULONGLONG function](..\propsys\nf-propsys-pspropertybag_writeulonglong.md) | Sets the ULONGLONG value of a property in a property bag. |
| [PSPropertyBag_WriteUnknown function](..\propsys\nf-propsys-pspropertybag_writeunknown.md) | Writes a property of an unknown data value in a property bag. |
| [PSPropertyKeyFromString function](..\propsys\nf-propsys-pspropertykeyfromstring.md) | Converts a string to a PROPERTYKEY structure. |
| [PSRefreshPropertySchema function](..\propsys\nf-propsys-psrefreshpropertyschema.md) | Not supported.It is valid to call this function, but it is not implemented to perform any function so there is no reason to do so. |
| [PSRegisterPropertySchema function](..\propsys\nf-propsys-psregisterpropertyschema.md) | Informs the schema subsystem of the addition of a property description schema file. |
| [PSSetPropertyValue function](..\propsys\nf-propsys-pssetpropertyvalue.md) | Sets the value of a property in a property store. |
| [PSStringFromPropertyKey function](..\propsys\nf-propsys-psstringfrompropertykey.md) | Creates a string that identifies a property from that property's key. |
| [PSUnregisterPropertySchema function](..\propsys\nf-propsys-psunregisterpropertyschema.md) | Informs the schema subsystem of the removal of a property description schema file. |
| [PropVariantChangeType function](..\propvarutil\nf-propvarutil-propvariantchangetype.md) | Coerces a value stored as a PROPVARIANT structure to an equivalent value of a different variant type. |
| [PropVariantClear function](..\propidl\nf-propidl-propvariantclear.md) | Clears a PROPVARIANT structure. |
| [PropVariantCompare function](..\propvarutil\nf-propvarutil-propvariantcompare.md) | Compares two PROPVARIANT structures, based on default comparison units and settings. |
| [PropVariantCompareEx function](..\propvarutil\nf-propvarutil-propvariantcompareex.md) | Extends PropVariantCompare by allowing the caller to compare two PROPVARIANT structures based on specified comparison units and flags. |
| [PropVariantCopy function](..\propidl\nf-propidl-propvariantcopy.md) | Creates a copy of a PROPVARIANT structure. |
| [PropVariantGetBooleanElem function](..\propvarutil\nf-propvarutil-propvariantgetbooleanelem.md) | Extracts a single Boolean element from a PROPVARIANT structure of type VT_BOOL, VT_VECTOR | VT_BOOL, or VT_ARRAY | VT_BOOL. |
| [PropVariantGetDoubleElem function](..\propvarutil\nf-propvarutil-propvariantgetdoubleelem.md) | Extracts a single double element from a PROPVARIANT structure of type VT_R8, VT_VECTOR | VT_R8, or VT_ARRAY | VT_R8. |
| [PropVariantGetElem function](..\propvarutil\nf-propvarutil-propvariantgetelem.md) | Initializes a PROPVARIANT structure based on a specified element in another PROPVARIANT structure. |
| [PropVariantGetElementCount function](..\propvarutil\nf-propvarutil-propvariantgetelementcount.md) | Retrieves the element count of a PROPVARIANT structure. |
| [PropVariantGetFileTimeElem function](..\propvarutil\nf-propvarutil-propvariantgetfiletimeelem.md) | Extracts a single FILETIME element from a PROPVARIANT structure of type VT_FILETIME, VT_VECTOR | VT_FILETIME, or VT_ARRAY | VT_FILETIME. |
| [PropVariantGetInt16Elem function](..\propvarutil\nf-propvarutil-propvariantgetint16elem.md) | Extracts a single Int16 element from a PROPVARIANT structure of type VT_I2, VT_VECTOR | VT_I2, or VT_ARRAY | VT_I2. |
| [PropVariantGetInt32Elem function](..\propvarutil\nf-propvarutil-propvariantgetint32elem.md) | Extracts a single Int32 element from a PROPVARIANT of type VT_I4, VT_VECTOR | VT_I4, or VT_ARRAY | VT_I4. |
| [PropVariantGetInt64Elem function](..\propvarutil\nf-propvarutil-propvariantgetint64elem.md) | Extracts a single Int64 element from a PROPVARIANT structure of type VT_I8, VT_VECTOR | VT_I8, or VT_ARRAY | VT_I8. |
| [PropVariantGetStringElem function](..\propvarutil\nf-propvarutil-propvariantgetstringelem.md) | Extracts a single Unicode string element from a PROPVARIANT structure of type VT_LPWSTR, VT_BSTR, VT_VECTOR | VT_LPWSTR, VT_VECTOR | VT_BSTR, or VT_ARRAY | VT_BSTR. |
| [PropVariantGetUInt16Elem function](..\propvarutil\nf-propvarutil-propvariantgetuint16elem.md) | Extracts a single unsigned Int16 element from a PROPVARIANT structure of type VT_U12, VT_VECTOR | VT_U12, or VT_ARRAY | VT_U12. |
| [PropVariantGetUInt32Elem function](..\propvarutil\nf-propvarutil-propvariantgetuint32elem.md) | Extracts a single unsigned Int32 element from a PROPVARIANT structure of type VT_UI4, VT_VECTOR | VT_UI4, or VT_ARRAY | VT_UI4. |
| [PropVariantGetUInt64Elem function](..\propvarutil\nf-propvarutil-propvariantgetuint64elem.md) | Extracts a single unsigned Int64 element from a PROPVARIANT structure of type VT_UI8, VT_VECTOR | VT_UI8, or VT_ARRAY | VT_UI8. |
| [PropVariantToBSTR function](..\propvarutil\nf-propvarutil-propvarianttobstr.md) | Extracts the BSTR property value of a PROPVARIANT structure. |
| [PropVariantToBoolean function](..\propvarutil\nf-propvarutil-propvarianttoboolean.md) | Extracts a Boolean property value of a PROPVARIANT structure. If no value can be extracted, then a default value is assigned. |
| [PropVariantToBooleanVector function](..\propvarutil\nf-propvarutil-propvarianttobooleanvector.md) | Extracts a Boolean vector from a PROPVARIANT structure. |
| [PropVariantToBooleanVectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttobooleanvectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly allocated Boolean vector. |
| [PropVariantToBooleanWithDefault function](..\propvarutil\nf-propvarutil-propvarianttobooleanwithdefault.md) | Extracts the Boolean property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned. |
| [PropVariantToBuffer function](..\propvarutil\nf-propvarutil-propvarianttobuffer.md) | Extracts the buffer value from a PROPVARIANT structure of type VT_VECTOR | VT_UI1 or VT_ARRRAY | VT_UI1. |
| [PropVariantToCLSID function](..\propvarutil\nf-propvarutil-propvarianttoclsid.md) | Extracts class identifier (CLSID) property value of a PROPVARIANT structure. |
| [PropVariantToDouble function](..\propvarutil\nf-propvarutil-propvarianttodouble.md) | Extracts double value from a PROPVARIANT structure. |
| [PropVariantToDoubleVector function](..\propvarutil\nf-propvarutil-propvarianttodoublevector.md) | Extracts a vector of doubles from a PROPVARIANT structure. |
| [PropVariantToDoubleVectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttodoublevectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated double vector. |
| [PropVariantToDoubleWithDefault function](..\propvarutil\nf-propvarutil-propvarianttodoublewithdefault.md) | Extracts a double property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned. |
| [PropVariantToFileTime function](..\propvarutil\nf-propvarutil-propvarianttofiletime.md) | Extracts the FILETIME structure from a PROPVARIANT structure. |
| [PropVariantToFileTimeVector function](..\propvarutil\nf-propvarutil-propvarianttofiletimevector.md) | Extracts data from a PROPVARIANT structure into a FILETIME vector. |
| [PropVariantToFileTimeVectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttofiletimevectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated FILETIME vector. |
| [PropVariantToGUID function](..\propvarutil\nf-propvarutil-propvarianttoguid.md) | Extracts a GUID value from a PROPVARIANT structure. |
| [PropVariantToInt16 function](..\propvarutil\nf-propvarutil-propvarianttoint16.md) | Extracts an Int16 property value of a PROPVARIANT structure. |
| [PropVariantToInt16Vector function](..\propvarutil\nf-propvarutil-propvarianttoint16vector.md) | Extracts a vector of Int16 values from a PROPVARIANT structure. |
| [PropVariantToInt16VectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttoint16vectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly allocated Int16 vector. |
| [PropVariantToInt16WithDefault function](..\propvarutil\nf-propvarutil-propvarianttoint16withdefault.md) | Extracts the Int16 property value of a PROPVARIANT structure. If no value currently exists, then specified default value is returned. |
| [PropVariantToInt32 function](..\propvarutil\nf-propvarutil-propvarianttoint32.md) | Extracts the Int32 property value of a PROPVARIANT structure. If no value can be extracted, then a default value is assigned. |
| [PropVariantToInt32Vector function](..\propvarutil\nf-propvarutil-propvarianttoint32vector.md) | Extracts a vector of long values from a PROPVARIANT structure. |
| [PropVariantToInt32VectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttoint32vectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated Int32 vector. |
| [PropVariantToInt32WithDefault function](..\propvarutil\nf-propvarutil-propvarianttoint32withdefault.md) | Extracts an Int32 value from a PROPVARIANT structure. If no value currently exists, then the specified default value is returned. |
| [PropVariantToInt64 function](..\propvarutil\nf-propvarutil-propvarianttoint64.md) | Extracts a LONGLONG value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned. |
| [PropVariantToInt64Vector function](..\propvarutil\nf-propvarutil-propvarianttoint64vector.md) | Extracts data from a PROPVARIANT structure into an Int64 vector. |
| [PropVariantToInt64VectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttoint64vectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated LONGLONG vector. |
| [PropVariantToInt64WithDefault function](..\propvarutil\nf-propvarutil-propvarianttoint64withdefault.md) | Extracts the Int64 property value of a PROPVARIANT structure. If no value exists, then specified default value is returned. |
| [PropVariantToStrRet function](..\propvarutil\nf-propvarutil-propvarianttostrret.md) | Extracts a string from a PROPVARIANT structure and places it into a STRRET structure. |
| [PropVariantToString function](..\propvarutil\nf-propvarutil-propvarianttostring.md) | Extracts a string value from a PROPVARIANT structure. |
| [PropVariantToStringAlloc function](..\propvarutil\nf-propvarutil-propvarianttostringalloc.md) | Extracts a string property value from a PROPVARIANT structure. |
| [PropVariantToStringVector function](..\propvarutil\nf-propvarutil-propvarianttostringvector.md) | Extracts a vector of strings from a PROPVARIANT structure. |
| [PropVariantToStringVectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttostringvectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly allocated strings in a newly allocated vector. |
| [PropVariantToStringWithDefault function](..\propvarutil\nf-propvarutil-propvarianttostringwithdefault.md) | Extracts the string property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned. |
| [PropVariantToUInt16 function](..\propvarutil\nf-propvarutil-propvarianttouint16.md) | Extracts a unsigned short value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned. |
| [PropVariantToUInt16Vector function](..\propvarutil\nf-propvarutil-propvarianttouint16vector.md) | Extracts data from a PROPVARIANT structure into an unsigned short vector. |
| [PropVariantToUInt16VectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttouint16vectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated unsigned short vector. |
| [PropVariantToUInt16WithDefault function](..\propvarutil\nf-propvarutil-propvarianttouint16withdefault.md) | Extracts an unsigned short value from a PROPVARIANT structure. If no value exists, then the specified default value is returned. |
| [PropVariantToUInt32 function](..\propvarutil\nf-propvarutil-propvarianttouint32.md) | Extracts an ULONG value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned. |
| [PropVariantToUInt32Vector function](..\propvarutil\nf-propvarutil-propvarianttouint32vector.md) | Extracts data from a PROPVARIANT structure into an ULONG vector. |
| [PropVariantToUInt32VectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttouint32vectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated ULONG vector. |
| [PropVariantToUInt32WithDefault function](..\propvarutil\nf-propvarutil-propvarianttouint32withdefault.md) | Extracts a ULONG value from a PROPVARIANT structure. If no value exists, then a specified default value is returned. |
| [PropVariantToUInt64 function](..\propvarutil\nf-propvarutil-propvarianttouint64.md) | Extracts a UInt64 value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned. |
| [PropVariantToUInt64Vector function](..\propvarutil\nf-propvarutil-propvarianttouint64vector.md) | Extracts data from a PROPVARIANT structure into a ULONGLONG vector. |
| [PropVariantToUInt64VectorAlloc function](..\propvarutil\nf-propvarutil-propvarianttouint64vectoralloc.md) | Extracts data from a PROPVARIANT structure into a newly-allocated ULONGLONG vector. |
| [PropVariantToUInt64WithDefault function](..\propvarutil\nf-propvarutil-propvarianttouint64withdefault.md) | Extracts ULONGLONG value from a PROPVARIANT structure. If no value exists, then the specified default value is returned. |
| [PropVariantToVariant function](..\propvarutil\nf-propvarutil-propvarianttovariant.md) | Converts the contents of a PROPVARIANT structure to a VARIANT structure. |
| [PropVariantToWinRTPropertyValue function](..\propsys\nf-propsys-propvarianttowinrtpropertyvalue.md) | Extracts data from a PROPVARIANT structure into a Windows Runtime property value. |
| [SHGetPropertyStoreFromIDList function](..\shobjidl_core\nf-shobjidl_core-shgetpropertystorefromidlist.md) | Retrieves an object that supports IPropertyStore or related interfaces from a pointer to an item identifier list (PIDL). |
| [SHGetPropertyStoreFromParsingName function](..\shobjidl_core\nf-shobjidl_core-shgetpropertystorefromparsingname.md) | Returns a property store for an item, given a path or parsing name. |
| [VariantCompare function](..\propvarutil\nf-propvarutil-variantcompare.md) | Compares two variant structures, based on default comparison rules. |
| [VariantGetBooleanElem function](..\propvarutil\nf-propvarutil-variantgetbooleanelem.md) | Extracts a single Boolean element from a variant structure. |
| [VariantGetDoubleElem function](..\propvarutil\nf-propvarutil-variantgetdoubleelem.md) | Extracts one double element from a variant structure. |
| [VariantGetElem function](..\propvarutil\nf-propvarutil-variantgetelem.md) | Initializes a VARIANT structure from a specified variant element. |
| [VariantGetElementCount function](..\propvarutil\nf-propvarutil-variantgetelementcount.md) | Retrieves the element count of a variant structure. |
| [VariantGetInt16Elem function](..\propvarutil\nf-propvarutil-variantgetint16elem.md) | Extracts a single Int16 element from a variant structure. |
| [VariantGetInt32Elem function](..\propvarutil\nf-propvarutil-variantgetint32elem.md) | Extracts a single Int32 element from a variant structure. |
| [VariantGetInt64Elem function](..\propvarutil\nf-propvarutil-variantgetint64elem.md) | Extracts a single Int64 element from a variant structure. |
| [VariantGetStringElem function](..\propvarutil\nf-propvarutil-variantgetstringelem.md) | Extracts a single wide string element from a variant structure. |
| [VariantGetUInt16Elem function](..\propvarutil\nf-propvarutil-variantgetuint16elem.md) | Extracts a single unsigned Int16 element from a variant structure. |
| [VariantGetUInt32Elem function](..\propvarutil\nf-propvarutil-variantgetuint32elem.md) | Extracts a single unsigned Int32 element from a variant structure. |
| [VariantGetUInt64Elem function](..\propvarutil\nf-propvarutil-variantgetuint64elem.md) | Extracts a single unsigned Int64 element from a variant structure. |
| [VariantToBoolean function](..\propvarutil\nf-propvarutil-varianttoboolean.md) | Extracts the value of a Boolean property from a VARIANT structure. If no value can be extracted, then a default value is assigned. |
| [VariantToBooleanArray function](..\propvarutil\nf-propvarutil-varianttobooleanarray.md) | Extracts an array of Boolean values from a VARIANT structure. |
| [VariantToBooleanArrayAlloc function](..\propvarutil\nf-propvarutil-varianttobooleanarrayalloc.md) | Allocates an array of BOOL values then extracts data from a VARIANT structure into that array. |
| [VariantToBooleanWithDefault function](..\propvarutil\nf-propvarutil-varianttobooleanwithdefault.md) | Extracts a BOOL value from a VARIANT structure. If no value exists, then the specified default value is returned. |
| [VariantToBuffer function](..\propvarutil\nf-propvarutil-varianttobuffer.md) | Extracts the contents of a buffer stored in a VARIANT structure of type VT_ARRRAY | VT_UI1. |
| [VariantToDosDateTime function](..\propvarutil\nf-propvarutil-varianttodosdatetime.md) | Extracts a date and time value in Microsoft MS-DOS format from a VARIANT structure. |
| [VariantToDouble function](..\propvarutil\nf-propvarutil-varianttodouble.md) | Extracts a DOUBLE value from a VARIANT structure. If no value can be extracted, then a default value is assigned. |
| [VariantToDoubleArray function](..\propvarutil\nf-propvarutil-varianttodoublearray.md) | Extracts an array of DOUBLE values from a VARIANT structure. |
| [VariantToDoubleArrayAlloc function](..\propvarutil\nf-propvarutil-varianttodoublearrayalloc.md) | Allocates an array of DOUBLE values then extracts data from a VARIANT structure into that array. |
| [VariantToDoubleWithDefault function](..\propvarutil\nf-propvarutil-varianttodoublewithdefault.md) | Extracts a DOUBLE value from a VARIANT structure. If no value exists, then the specified default value is returned. |
| [VariantToFileTime function](..\propvarutil\nf-propvarutil-varianttofiletime.md) | Extracts a FILETIME structure from a variant structure. |
| [VariantToGUID function](..\propvarutil\nf-propvarutil-varianttoguid.md) | Extracts a GUID property value of a variant structure. |
| [VariantToInt16 function](..\propvarutil\nf-propvarutil-varianttoint16.md) | Extracts the Int16 property value of a variant structure. If no value can be extracted, then a default value is assigned by this function. |
| [VariantToInt16Array function](..\propvarutil\nf-propvarutil-varianttoint16array.md) | Extracts data from a vector structure into an Int16 array. |
| [VariantToInt16ArrayAlloc function](..\propvarutil\nf-propvarutil-varianttoint16arrayalloc.md) | Extracts data from a vector structure into a newly-allocated Int16 array. |
| [VariantToInt16WithDefault function](..\propvarutil\nf-propvarutil-varianttoint16withdefault.md) | Extracts an Int16 property value of a variant structure. If no value exists, then the specified default value is returned. |
| [VariantToInt32 function](..\propvarutil\nf-propvarutil-varianttoint32.md) | Extracts an Int32 property value of a variant structure. If no value can be extracted, then a default value is assigned. |
| [VariantToInt32Array function](..\propvarutil\nf-propvarutil-varianttoint32array.md) | Extracts data from a vector structure into an Int32 array. |
| [VariantToInt32ArrayAlloc function](..\propvarutil\nf-propvarutil-varianttoint32arrayalloc.md) | Extracts data from a vector structure into a newly-allocated Int32 array. |
| [VariantToInt32WithDefault function](..\propvarutil\nf-propvarutil-varianttoint32withdefault.md) | Extracts an Int32 property value of a variant structure. If no value exists, then the specified default value is returned. |
| [VariantToInt64 function](..\propvarutil\nf-propvarutil-varianttoint64.md) | Extracts an Int64 property value of a variant structure. If no value can be extracted, then a default value is assigned. |
| [VariantToInt64Array function](..\propvarutil\nf-propvarutil-varianttoint64array.md) | Extracts data from a vector structure into an Int64 array. |
| [VariantToInt64ArrayAlloc function](..\propvarutil\nf-propvarutil-varianttoint64arrayalloc.md) | Extracts data from a vector structure into a newly-allocated Int64 array. |
| [VariantToInt64WithDefault function](..\propvarutil\nf-propvarutil-varianttoint64withdefault.md) | Extracts an Int64 property value of a variant structure. If no value exists, then the specified default value is returned. |
| [VariantToPropVariant function](..\propvarutil\nf-propvarutil-varianttopropvariant.md) | Copies the contents of a VARIANT structure to a PROPVARIANT structure. |
| [VariantToStrRet function](..\propvarutil\nf-propvarutil-varianttostrret.md) | If the source variant is a VT_BSTR, extracts string and places it into a STRRET structure. |
| [VariantToString function](..\propvarutil\nf-propvarutil-varianttostring.md) | Extracts the variant value of a variant structure to a string. If no value can be extracted, then a default value is assigned. |
| [VariantToStringAlloc function](..\propvarutil\nf-propvarutil-varianttostringalloc.md) | Extracts the variant value of a variant structure to a newly-allocated string. If no value can be extracted, then a default value is assigned. |
| [VariantToStringArray function](..\propvarutil\nf-propvarutil-varianttostringarray.md) | Extracts data from a vector structure into a String array. |
| [VariantToStringArrayAlloc function](..\propvarutil\nf-propvarutil-varianttostringarrayalloc.md) | Extracts data from a vector structure into a newly-allocated String array. |
| [VariantToStringWithDefault function](..\propvarutil\nf-propvarutil-varianttostringwithdefault.md) | Extracts the string property value of a variant structure. If no value exists, then the specified default value is returned. |
| [VariantToUInt16 function](..\propvarutil\nf-propvarutil-varianttouint16.md) | Extracts an unsigned Int16 property value of a variant structure. If no value can be extracted, then a default value is assigned by this function. |
| [VariantToUInt16Array function](..\propvarutil\nf-propvarutil-varianttouint16array.md) | Extracts data from a vector structure into an unsigned Int16 array. |
| [VariantToUInt16ArrayAlloc function](..\propvarutil\nf-propvarutil-varianttouint16arrayalloc.md) | Extracts data from a vector structure into a newly-allocated unsigned Int16 array. |
| [VariantToUInt16WithDefault function](..\propvarutil\nf-propvarutil-varianttouint16withdefault.md) | Extracts an unsigned Int16 property value of a variant structure. If no value exists, then the specified default value is returned. |
| [VariantToUInt32 function](..\propvarutil\nf-propvarutil-varianttouint32.md) | Extracts unsigned Int32 property value of a variant structure. If no value can be extracted, then a default value is assigned. |
| [VariantToUInt32Array function](..\propvarutil\nf-propvarutil-varianttouint32array.md) | Extracts data from a vector structure into an unsigned Int32 array. |
| [VariantToUInt32ArrayAlloc function](..\propvarutil\nf-propvarutil-varianttouint32arrayalloc.md) | Extracts data from a vector structure into a newly-allocated unsigned Int32 array. |
| [VariantToUInt32WithDefault function](..\propvarutil\nf-propvarutil-varianttouint32withdefault.md) | Extracts an unsigned Int32 property value of a variant structure. If no value currently exists, then the specified default value is returned. |
| [VariantToUInt64 function](..\propvarutil\nf-propvarutil-varianttouint64.md) | Extracts unsigned Int64 property value of a variant structure. If no value can be extracted, then a default value is assigned. |
| [VariantToUInt64Array function](..\propvarutil\nf-propvarutil-varianttouint64array.md) | Extracts data from a vector structure into an unsigned Int64 array. |
| [VariantToUInt64ArrayAlloc function](..\propvarutil\nf-propvarutil-varianttouint64arrayalloc.md) | Extracts data from a vector structure into a newly-allocated unsigned Int64 array. |
| [VariantToUInt64WithDefault function](..\propvarutil\nf-propvarutil-varianttouint64withdefault.md) | Extracts an unsigned Int64 property value of a variant structure. If no value currently exists, then the specified default value is returned. |
| [WinRTPropertyValueToPropVariant function](..\propsys\nf-propsys-winrtpropertyvaluetopropvariant.md) | Copies the content from a Windows runtime property value to a PROPVARIANT structure. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [GETPROPERTYSTOREFLAGS enumeration](..\propsys\ne-propsys-getpropertystoreflags.md) | Indicates flags that modify the property store object retrieved by methods that create a property store, such as IShellItem2 |
| [PDOPSTATUS enumeration](..\shobjidl_core\ne-shobjidl_core-pdopstatus.md) | Provides operation status flags. |
| [PKA_FLAGS enumeration](..\propsys\ne-propsys-pka_flags.md) | Describes property change array behavior. |
| [PLACEHOLDER_STATES enumeration](..\shobjidl_core\ne-shobjidl_core-placeholder_states.md) | Specifies the states that a placeholder file can have. Retrieve this value through the System.FilePlaceholderStatus (PKEY_FilePlaceholderStatus) property. |
| [PROPDESC_AGGREGATION_TYPE enumeration](..\propsys\ne-propsys-propdesc_aggregation_type.md) | Describes how property values are displayed when multiple items are selected. |
| [PROPDESC_COLUMNINDEX_TYPE enumeration](..\propsys\ne-propsys-propdesc_columnindex_type.md) | Indicates whether or how a property can be indexed. |
| [PROPDESC_CONDITION_TYPE enumeration](..\propsys\ne-propsys-propdesc_condition_type.md) | Describes the condition type to use when displaying the property in the query builder UI in Windows Vista, but not in Windows 7 and later. |
| [PROPDESC_ENUMFILTER enumeration](..\propsys\ne-propsys-propdesc_enumfilter.md) | Describes the filtered list of property descriptions that is returned. |
| [PROPDESC_FORMAT_FLAGS enumeration](..\propsys\ne-propsys-propdesc_format_flags.md) | Used by property description helper functions, such as PSFormatForDisplay, to indicate the format of a property string. |
| [PROPDESC_RELATIVEDESCRIPTION_TYPE enumeration](..\propsys\ne-propsys-propdesc_relativedescription_type.md) | Describes the relative description type for a property description, as determined by the relativeDescriptionType attribute of the displayInfo element. |
| [PROPDESC_SEARCHINFO_FLAGS enumeration](..\propsys\ne-propsys-propdesc_searchinfo_flags.md) | Determines whether and how a property is indexed by Windows Search. |
| [PROPDESC_TYPE_FLAGS enumeration](..\propsys\ne-propsys-propdesc_type_flags.md) | Describes attributes of the typeInfo element in the property's .propdesc file. |
| [PROPDESC_VIEW_FLAGS enumeration](..\propsys\ne-propsys-propdesc_view_flags.md) | These flags describe properties in property description list strings. |
| [PROPVAR_COMPARE_UNIT enumeration](..\propvarutil\ne-propvarutil-propvar_compare_unit.md) | These flags are associated with certain PROPVARIANT structure comparisons. |
| [PSC_STATE enumeration](..\propsys\ne-propsys-psc_state.md) | Specifies the state of a property. They are set manually by the code that is hosting the in-memory property store cache. |
| [SYNC_TRANSFER_STATUS enumeration](..\shobjidl_core\ne-shobjidl_core-sync_transfer_status.md) | Specifies possible status values used in the System.SyncTransferStatus property. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IPropertyChange interface](..\propsys\nn-propsys-ipropertychange.md) | Exposes a method that encapsulates a change to a single property. |
| [IPropertyChangeArray interface](..\propsys\nn-propsys-ipropertychangearray.md) | Exposes methods for several multiple change operations that may be passed to IFileOperation. |
| [IPropertyDescription interface](..\propsys\nn-propsys-ipropertydescription.md) | Exposes methods that enumerate and retrieve individual property description details. |
| [IPropertyDescription2 interface](..\propsys\nn-propsys-ipropertydescription2.md) | Exposes methods that enumerate and retrieve individual property description details. |
| [IPropertyDescriptionAliasInfo interface](..\propsys\nn-propsys-ipropertydescriptionaliasinfo.md) | Exposes methods to get the &#0034;sort by&#0034; columns properties for an item. This interface is used by UI objects that want to retrieve the primary or secondary sort columns for a given property. |
| [IPropertyDescriptionList interface](..\propsys\nn-propsys-ipropertydescriptionlist.md) | Exposes methods that extract information from a collection of property descriptions presented as a list. |
| [IPropertyDescriptionRelatedPropertyInfo interface](..\propsys\nn-propsys-ipropertydescriptionrelatedpropertyinfo.md) | Provides a method that retrives an IPropertyDescription interface. |
| [IPropertyDescriptionSearchInfo interface](..\propsys\nn-propsys-ipropertydescriptionsearchinfo.md) | Exposes search-related information for a property. |
| [IPropertyEnumType interface](..\propsys\nn-propsys-ipropertyenumtype.md) | Exposes methods that extract data from enumeration information. IPropertyEnumType gives access to the enum and enumRange elements in the property schema in a programmatic way at run time. |
| [IPropertyEnumType2 interface](..\propsys\nn-propsys-ipropertyenumtype2.md) | Exposes methods that extract data from enumeration information. IPropertyEnumType2 extends IPropertyEnumType. |
| [IPropertyEnumTypeList interface](..\propsys\nn-propsys-ipropertyenumtypelist.md) | Exposes methods that enumerate the possible values for a property. |
| [IPropertyStoreCache interface](..\propsys\nn-propsys-ipropertystorecache.md) | Exposes methods that allow a handler to manage various states for each property. |
| [IPropertyStoreCapabilities interface](..\propsys\nn-propsys-ipropertystorecapabilities.md) | Exposes a method that determines whether a property can be edited in the UI by the user. |
| [IPropertyStoreFactory interface](..\propsys\nn-propsys-ipropertystorefactory.md) | Exposes methods to get an IPropertyStore object. |
| [IPropertySystem interface](..\propsys\nn-propsys-ipropertysystem.md) | Exposes methods that get property descriptions, register and unregister property schemas, enumerate property descriptions, and format property values in a type-strict way. |
| [IPropertyUI interface](..\shobjidl_core\nn-shobjidl_core-ipropertyui.md) | Developers should use IPropertyDescription instead. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IPropertyChange::ApplyToPropVariant](..\propsys\nf-propsys-ipropertychange-applytopropvariant.md) | Applies a change to a property value. |
| [IPropertyChangeArray::AppendOrReplace](..\propsys\nf-propsys-ipropertychangearray-appendorreplace.md) | Replaces the first occurrence of a change that affects the same property key as the provided change. If the property key is not already in the array, this method appends the change to the end of the array. |
| [IPropertyChangeArray::Append](..\propsys\nf-propsys-ipropertychangearray-append.md) | Inserts a change operation at the end of an array. |
| [IPropertyChangeArray::GetAt](..\propsys\nf-propsys-ipropertychangearray-getat.md) | Gets the change operation at a specified array index. |
| [IPropertyChangeArray::GetCount](..\propsys\nf-propsys-ipropertychangearray-getcount.md) | Gets the number of change operations in the array. |
| [IPropertyChangeArray::InsertAt](..\propsys\nf-propsys-ipropertychangearray-insertat.md) | Inserts a change operation into an array at the specified position. |
| [IPropertyChangeArray::IsKeyInArray](..\propsys\nf-propsys-ipropertychangearray-iskeyinarray.md) | Specifies whether a particular property key exists in the change array. |
| [IPropertyChangeArray::RemoveAt](..\propsys\nf-propsys-ipropertychangearray-removeat.md) | Removes a specified change. |
| [IPropertyDescription2::GetImageReferenceForValue](..\propsys\nf-propsys-ipropertydescription2-getimagereferenceforvalue.md) | Gets the image reference associated with a property value. |
| [IPropertyDescription::CoerceToCanonicalValue](..\propsys\nf-propsys-ipropertydescription-coercetocanonicalvalue.md) | Coerces the value to the canonical value, according to the property description. |
| [IPropertyDescription::FormatForDisplay](..\propsys\nf-propsys-ipropertydescription-formatfordisplay.md) | Gets a formatted, Unicode string representation of a property value. |
| [IPropertyDescription::GetAggregationType](..\propsys\nf-propsys-ipropertydescription-getaggregationtype.md) | Gets a value that describes how the property values are displayed when multiple items are selected in the UI. |
| [IPropertyDescription::GetCanonicalName](..\propsys\nf-propsys-ipropertydescription-getcanonicalname.md) | Gets the case-sensitive name by which a property is known to the system, regardless of its localized name. |
| [IPropertyDescription::GetColumnState](..\propsys\nf-propsys-ipropertydescription-getcolumnstate.md) | Gets the column state flag, which describes how the property should be treated by interfaces or APIs that use this flag. |
| [IPropertyDescription::GetConditionType](..\propsys\nf-propsys-ipropertydescription-getconditiontype.md) | Gets the condition type and default condition operation to use when displaying the property in the query builder UI. This influences the list of predicate conditions (for example, equals, less than, and contains) that are shown for this property. |
| [IPropertyDescription::GetDefaultColumnWidth](..\propsys\nf-propsys-ipropertydescription-getdefaultcolumnwidth.md) | Gets the default column width of the property in a list view. |
| [IPropertyDescription::GetDisplayName](..\propsys\nf-propsys-ipropertydescription-getdisplayname.md) | Gets the display name of the property as it is shown in any UI. |
| [IPropertyDescription::GetDisplayType](..\propsys\nf-propsys-ipropertydescription-getdisplaytype.md) | Gets the current data type used to display the property. |
| [IPropertyDescription::GetEditInvitation](..\propsys\nf-propsys-ipropertydescription-geteditinvitation.md) | Gets the text used in edit controls hosted in various dialog boxes. |
| [IPropertyDescription::GetEnumTypeList](..\propsys\nf-propsys-ipropertydescription-getenumtypelist.md) | Gets an instance of an IPropertyEnumTypeList, which can be used to enumerate the possible values for a property. |
| [IPropertyDescription::GetGroupingRange](..\propsys\nf-propsys-ipropertydescription-getgroupingrange.md) | Gets the grouping method to be used when a view is grouped by a property, and retrieves the grouping type. |
| [IPropertyDescription::GetPropertyKey](..\propsys\nf-propsys-ipropertydescription-getpropertykey.md) | Gets a structure that acts as a property's unique identifier. |
| [IPropertyDescription::GetPropertyType](..\propsys\nf-propsys-ipropertydescription-getpropertytype.md) | Gets the variant type of the property. |
| [IPropertyDescription::GetRelativeDescriptionType](..\propsys\nf-propsys-ipropertydescription-getrelativedescriptiontype.md) | Gets the relative description type for a property description. |
| [IPropertyDescription::GetRelativeDescription](..\propsys\nf-propsys-ipropertydescription-getrelativedescription.md) | Compares two property values in the manner specified by the property description. Returns two display strings that describe how the two properties compare. |
| [IPropertyDescription::GetSortDescriptionLabel](..\propsys\nf-propsys-ipropertydescription-getsortdescriptionlabel.md) | Gets the localized display string that describes the current sort order. |
| [IPropertyDescription::GetSortDescription](..\propsys\nf-propsys-ipropertydescription-getsortdescription.md) | Gets the current sort description flags for the property, which indicate the particular wordings of sort offerings. |
| [IPropertyDescription::GetTypeFlags](..\propsys\nf-propsys-ipropertydescription-gettypeflags.md) | Gets a set of flags that describe the uses and capabilities of the property. |
| [IPropertyDescription::GetViewFlags](..\propsys\nf-propsys-ipropertydescription-getviewflags.md) | Gets the current set of flags governing the property's view. |
| [IPropertyDescription::IsValueCanonical](..\propsys\nf-propsys-ipropertydescription-isvaluecanonical.md) | Gets a value that indicates whether a property is canonical according to the definition of the property description. |
| [IPropertyDescriptionAliasInfo::GetAdditionalSortByAliases](..\propsys\nf-propsys-ipropertydescriptionaliasinfo-getadditionalsortbyaliases.md) | Gets the address of a pointer to the IPropertyDescriptionList interface, which contains additional sort column values. |
| [IPropertyDescriptionAliasInfo::GetSortByAlias](..\propsys\nf-propsys-ipropertydescriptionaliasinfo-getsortbyalias.md) | Gets the address of a pointer to the IPropertyDescription interface containing the primary sort column. |
| [IPropertyDescriptionList::GetAt](..\propsys\nf-propsys-ipropertydescriptionlist-getat.md) | Gets the property description at the specified index in a property description list. |
| [IPropertyDescriptionList::GetCount](..\propsys\nf-propsys-ipropertydescriptionlist-getcount.md) | Gets the number of properties included in the property list. |
| [IPropertyDescriptionRelatedPropertyInfo::GetRelatedProperty](..\propsys\nf-propsys-ipropertydescriptionrelatedpropertyinfo-getrelatedproperty.md) | Retrieves an IPropertyDescription object that represents the related property. |
| [IPropertyDescriptionSearchInfo::GetColumnIndexType](..\propsys\nf-propsys-ipropertydescriptionsearchinfo-getcolumnindextype.md) | Determines the how the current property is indexed. |
| [IPropertyDescriptionSearchInfo::GetMaxSize](..\propsys\nf-propsys-ipropertydescriptionsearchinfo-getmaxsize.md) | Gets the maximum size value from the property schema's searchInfo element. |
| [IPropertyDescriptionSearchInfo::GetProjectionString](..\propsys\nf-propsys-ipropertydescriptionsearchinfo-getprojectionstring.md) | Returns a pointer to a string containing the canonical name of the item. |
| [IPropertyDescriptionSearchInfo::GetSearchInfoFlags](..\propsys\nf-propsys-ipropertydescriptionsearchinfo-getsearchinfoflags.md) | Gets the PROPDESC_SEARCHINFO_FLAGS associated with the property. |
| [IPropertyEnumType2::GetImageReference](..\propsys\nf-propsys-ipropertyenumtype2-getimagereference.md) | Retrieves the image reference associated with a property enumeration. |
| [IPropertyEnumType::GetDisplayText](..\propsys\nf-propsys-ipropertyenumtype-getdisplaytext.md) | Gets display text from an enumeration information structure. |
| [IPropertyEnumType::GetEnumType](..\propsys\nf-propsys-ipropertyenumtype-getenumtype.md) | Gets an enumeration type from an enumeration information structure. |
| [IPropertyEnumType::GetRangeMinValue](..\propsys\nf-propsys-ipropertyenumtype-getrangeminvalue.md) | Gets a minimum value from an enumeration information structure. |
| [IPropertyEnumType::GetRangeSetValue](..\propsys\nf-propsys-ipropertyenumtype-getrangesetvalue.md) | Gets a set value from an enumeration information structure. |
| [IPropertyEnumType::GetValue](..\propsys\nf-propsys-ipropertyenumtype-getvalue.md) | Gets a value from an enumeration information structure. |
| [IPropertyEnumTypeList::FindMatchingIndex](..\propsys\nf-propsys-ipropertyenumtypelist-findmatchingindex.md) | Compares the specified property value against the enumerated values in a list and returns the matching index. |
| [IPropertyEnumTypeList::GetAt](..\propsys\nf-propsys-ipropertyenumtypelist-getat.md) | Gets the IPropertyEnumType object at the specified index in the list. |
| [IPropertyEnumTypeList::GetConditionAt](..\propsys\nf-propsys-ipropertyenumtypelist-getconditionat.md) | Not supported.Gets the condition at the specified index. |
| [IPropertyEnumTypeList::GetCount](..\propsys\nf-propsys-ipropertyenumtypelist-getcount.md) | Gets the number of elements in the list. |
| [IPropertyStoreCache::GetState](..\propsys\nf-propsys-ipropertystorecache-getstate.md) | Gets the state of a specified property key. |
| [IPropertyStoreCache::GetValueAndState](..\propsys\nf-propsys-ipropertystorecache-getvalueandstate.md) | Gets value and state data for a property key. |
| [IPropertyStoreCache::SetValueAndState](..\propsys\nf-propsys-ipropertystorecache-setvalueandstate.md) | Sets value and state data for a property key. |
| [IPropertyStoreCapabilities::IsPropertyWritable](..\propsys\nf-propsys-ipropertystorecapabilities-ispropertywritable.md) | Queries whether the property handler allows a specific property to be edited in the UI by the user. |
| [IPropertyStoreFactory::GetPropertyStoreForKeys](..\propsys\nf-propsys-ipropertystorefactory-getpropertystoreforkeys.md) | Gets an IPropertyStore object, given a set of property keys. This provides an alternative, possibly faster, method of getting an IPropertyStore object compared to calling IPropertyStoreFactory |
| [IPropertyStoreFactory::GetPropertyStore](..\propsys\nf-propsys-ipropertystorefactory-getpropertystore.md) | Gets an IPropertyStore object that corresponds to the supplied flags. |
| [IPropertySystem::EnumeratePropertyDescriptions](..\propsys\nf-propsys-ipropertysystem-enumeratepropertydescriptions.md) | Gets an instance of the subsystem object that implements IPropertyDescriptionList, to obtain either the entire or a partial list of property descriptions in the system. |
| [IPropertySystem::FormatForDisplayAlloc](..\propsys\nf-propsys-ipropertysystem-formatfordisplayalloc.md) | Gets a string representation of a property value to an allocated memory buffer. |
| [IPropertySystem::FormatForDisplay](..\propsys\nf-propsys-ipropertysystem-formatfordisplay.md) | Gets a formatted, Unicode string representation of a property value. |
| [IPropertySystem::GetPropertyDescriptionByName](..\propsys\nf-propsys-ipropertysystem-getpropertydescriptionbyname.md) | Gets an instance of the subsystem object that implements IPropertyDescription, to obtain the property description for a given canonical name. |
| [IPropertySystem::GetPropertyDescriptionListFromString](..\propsys\nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring.md) | Gets an instance of the subsystem object that implements IPropertyDescriptionList, to obtain an ordered collection of property descriptions, based on the provided string. |
| [IPropertySystem::GetPropertyDescription](..\propsys\nf-propsys-ipropertysystem-getpropertydescription.md) | Gets an instance of the subsystem object that implements IPropertyDescription, to obtain the property description for a given PROPERTYKEY. |
| [IPropertySystem::RefreshPropertySchema](..\propsys\nf-propsys-ipropertysystem-refreshpropertyschema.md) | Not supported. |
| [IPropertySystem::RegisterPropertySchema](..\propsys\nf-propsys-ipropertysystem-registerpropertyschema.md) | Informs the schema subsystem of the addition of a property description schema file. |
| [IPropertySystem::UnregisterPropertySchema](..\propsys\nf-propsys-ipropertysystem-unregisterpropertyschema.md) | Informs the schema subsystem of the removal of a property description schema (.propdesc) file, using a file path to the .propdesc file on the local machine. |
| [IPropertyUI::FormatForDisplay](..\shobjidl_core\nf-shobjidl_core-ipropertyui-formatfordisplay.md) | Developers should use IPropertyDescription instead. Gets a formatted, Unicode string representation of a property value. |
| [IPropertyUI::GetDefaultWidth](..\shobjidl_core\nf-shobjidl_core-ipropertyui-getdefaultwidth.md) | Developers should use IPropertyDescription instead. Gets the width of the property description. |
| [IPropertyUI::GetDisplayName](..\shobjidl_core\nf-shobjidl_core-ipropertyui-getdisplayname.md) | Developers should use IPropertyDescription instead. Gets a string specifying the name of the property suitable for display to users. |
| [IPropertyUI::GetFlags](..\shobjidl_core\nf-shobjidl_core-ipropertyui-getflags.md) | Developers should use IPropertyDescription instead. Gets property feature flags for a specified property. |
| [IPropertyUI::GetHelpInfo](..\shobjidl_core\nf-shobjidl_core-ipropertyui-gethelpinfo.md) | Developers should use IPropertyDescription instead. |
| [IPropertyUI::GetPropertyDescription](..\shobjidl_core\nf-shobjidl_core-ipropertyui-getpropertydescription.md) | Developers should use IPropertyDescription instead. Gets the property description of a specified property. |
| [IPropertyUI::ParsePropertyName](..\shobjidl_core\nf-shobjidl_core-ipropertyui-parsepropertyname.md) | Developers should use IPropertyDescription instead. Reads the characters of the specified property name and identifies the FMTID and PROPID of the property. |
