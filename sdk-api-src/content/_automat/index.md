---
UID: TP:automat
ms.assetid: fa0e9310-2f3a-3207-9d42-b2f8ad9f6315
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Automation



Overview of the Automation technology.

To develop Automation, you need these headers:

 * [oaidl.h](..\oaidl\index.md)
 * [oleauto.h](..\oleauto\index.md)
 * [olectl.h](..\olectl\index.md)
 * [wia_xp.h](..\wia_xp\index.md)
 * [wtypes.h](..\wtypes\index.md)

For the programming guide, see [Automation](/previous-versions/windows/desktop/automat).

## Functions

| Title   | Description   |
| ---- |:---- |
| [BSTR_UserFree function](..\oaidl\nf-oaidl-bstr_userfree.md) | Frees resources on the server side when called by RPC stub files. |
| [BSTR_UserFree64 function](..\oaidl\nf-oaidl-bstr_userfree64.md) | Frees resources on the server side when called by RPC stub files. |
| [BSTR_UserMarshal function](..\oaidl\nf-oaidl-bstr_usermarshal.md) | Marshals a BSTR object into the RPC buffer. |
| [BSTR_UserMarshal64 function](..\oaidl\nf-oaidl-bstr_usermarshal64.md) | Marshals a BSTR object into the RPC buffer. |
| [BSTR_UserSize function](..\oaidl\nf-oaidl-bstr_usersize.md) | Calculates the wire size of the BSTR object, and gets its handle and data. |
| [BSTR_UserSize64 function](..\oaidl\nf-oaidl-bstr_usersize64.md) | Calculates the wire size of the BSTR object, and gets its handle and data. |
| [BSTR_UserUnmarshal function](..\oaidl\nf-oaidl-bstr_userunmarshal.md) | Unmarshals a BSTR object from the RPC buffer. |
| [BSTR_UserUnmarshal64 function](..\oaidl\nf-oaidl-bstr_userunmarshal64.md) | Unmarshals a BSTR object from the RPC buffer. |
| [BstrFromVector function](..\oleauto\nf-oleauto-bstrfromvector.md) | Returns a BSTR, assigning each element of the vector to a character in the BSTR. |
| [ClearCustData function](..\oleauto\nf-oleauto-clearcustdata.md) | Releases memory used to hold the custom data item. |
| [CreateDispTypeInfo function](..\oleauto\nf-oleauto-createdisptypeinfo.md) | Creates simplified type information for use in an implementation of IDispatch. |
| [CreateErrorInfo function](..\oleauto\nf-oleauto-createerrorinfo.md) | Creates an instance of a generic error object. |
| [CreateStdDispatch function](..\oleauto\nf-oleauto-createstddispatch.md) | Creates a standard implementation of the IDispatch interface through a single function call. This simplifies exposing objects through Automation. |
| [CreateTypeLib function](..\oleauto\nf-oleauto-createtypelib.md) | Provides access to a new object instance that supports the ICreateTypeLib interface. |
| [CreateTypeLib2 function](..\oleauto\nf-oleauto-createtypelib2.md) | Creates a type library in the current file format. |
| [DispCallFunc function](..\oleauto\nf-oleauto-dispcallfunc.md) | Low-level helper for Invoke that provides machine independence for customized Invoke. |
| [DispGetIDsOfNames function](..\oleauto\nf-oleauto-dispgetidsofnames.md) | Low-level helper for Invoke that provides machine independence for customized Invoke. |
| [DispGetParam function](..\oleauto\nf-oleauto-dispgetparam.md) | Retrieves a parameter from the DISPPARAMS structure, checking both named parameters and positional parameters, and coerces the parameter to the specified type. |
| [DispInvoke function](..\oleauto\nf-oleauto-dispinvoke.md) | Automatically calls member functions on an interface, given the type information for the interface. |
| [DosDateTimeToVariantTime function](..\oleauto\nf-oleauto-dosdatetimetovarianttime.md) | Converts the MS-DOS representation of time to the date and time representation stored in a variant. |
| [GetActiveObject function](..\oleauto\nf-oleauto-getactiveobject.md) | Retrieves a pointer to a running object that has been registered with OLE. |
| [GetAltMonthNames function](..\oleauto\nf-oleauto-getaltmonthnames.md) | Retrieves the secondary (alternate) month names. |
| [GetErrorInfo function](..\oleauto\nf-oleauto-geterrorinfo.md) | Obtains the error information pointer set by the previous call to SetErrorInfo in the current logical thread. |
| [GetRecordInfoFromGuids function](..\oleauto\nf-oleauto-getrecordinfofromguids.md) | Returns a pointer to the IRecordInfo interface for a UDT by passing the GUID of the type information without having to load the type library. |
| [GetRecordInfoFromTypeInfo function](..\oleauto\nf-oleauto-getrecordinfofromtypeinfo.md) | Returns a pointer to the IRecordInfo interface of the UDT by passing its type information. |
| [LHashValOfNameSys function](..\oleauto\nf-oleauto-lhashvalofnamesys.md) | Computes a hash value for a name. |
| [LHashValOfNameSysA function](..\oleauto\nf-oleauto-lhashvalofnamesysa.md) | Computes a hash value for the specified name. |
| [LPSAFEARRAY_UserFree function](..\wia_xp\nf-wia_xp-lpsafearray_userfree.md) | Frees resources on the server side when called by RPC stub files. |
| [LPSAFEARRAY_UserFree64 function](..\wia_xp\nf-wia_xp-lpsafearray_userfree64.md) | Frees resources on the server side when called by RPC stub files. |
| [LPSAFEARRAY_UserMarshal function](..\wia_xp\nf-wia_xp-lpsafearray_usermarshal.md) | Marshals data from the specified SAFEARRAY object to the user's RPC buffer on the client or server side. |
| [LPSAFEARRAY_UserMarshal64 function](..\wia_xp\nf-wia_xp-lpsafearray_usermarshal64.md) | Marshals data from the specified SAFEARRAY object to the user's RPC buffer on the client or server side. |
| [LPSAFEARRAY_UserSize function](..\wia_xp\nf-wia_xp-lpsafearray_usersize.md) | Calculates the wire size of the SAFEARRAY object, and gets its handle and data. |
| [LPSAFEARRAY_UserSize64 function](..\wia_xp\nf-wia_xp-lpsafearray_usersize64.md) | Calculates the wire size of the SAFEARRAY object, and gets its handle and data. |
| [LPSAFEARRAY_UserUnmarshal function](..\wia_xp\nf-wia_xp-lpsafearray_userunmarshal.md) | Unmarshals a SAFEARRAY object from the RPC buffer. |
| [LPSAFEARRAY_UserUnmarshal64 function](..\wia_xp\nf-wia_xp-lpsafearray_userunmarshal64.md) | Unmarshals a SAFEARRAY object from the RPC buffer. |
| [LoadRegTypeLib function](..\oleauto\nf-oleauto-loadregtypelib.md) | Uses registry information to load a type library. |
| [LoadTypeLib function](..\oleauto\nf-oleauto-loadtypelib.md) | Loads and registers a type library. |
| [LoadTypeLibEx function](..\oleauto\nf-oleauto-loadtypelibex.md) | Loads a type library and (optionally) registers it in the system registry.  . |
| [OaBuildVersion function](..\oleauto\nf-oleauto-oabuildversion.md) | Retrieves the build version of OLE Automation. |
| [OaEnablePerUserTLibRegistration function](..\oleauto\nf-oleauto-oaenableperusertlibregistration.md) | Enables the RegisterTypeLib function to override default registry mappings under Windows Vista Service Pack 1 (SP1), Windows Server 2008, and later operating system versions. |
| [OleLoadPictureFile function](..\olectl\nf-olectl-oleloadpicturefile.md) | Creates an IPictureDisp object from a picture file on disk. |
| [OleLoadPictureFileEx function](..\olectl\nf-olectl-oleloadpicturefileex.md) | Loads a picture from a file. |
| [OleSavePictureFile function](..\olectl\nf-olectl-olesavepicturefile.md) | Saves a picture to a file. |
| [QueryPathOfRegTypeLib function](..\oleauto\nf-oleauto-querypathofregtypelib.md) | Retrieves the path of a registered type library. |
| [RegisterActiveObject function](..\oleauto\nf-oleauto-registeractiveobject.md) | Registers an object as the active object for its class. |
| [RegisterTypeLib function](..\oleauto\nf-oleauto-registertypelib.md) | Adds information about a type library to the system registry. |
| [RegisterTypeLibForUser function](..\oleauto\nf-oleauto-registertypelibforuser.md) | Registers a type library for use by the calling user. |
| [RevokeActiveObject function](..\oleauto\nf-oleauto-revokeactiveobject.md) | Ends an object's status as active. |
| [SafeArrayAccessData function](..\oleauto\nf-oleauto-safearrayaccessdata.md) | Increments the lock count of an array, and retrieves a pointer to the array data. |
| [SafeArrayAddRef function](..\oleauto\nf-oleauto-safearrayaddref.md) | Increases the pinning reference count of the descriptor for the specified safe array by one, and may increase the pinning reference count of the data for the specified safe array by one if that data was dynamically allocated, as determined by the descriptor of the safe array. |
| [SafeArrayAllocData function](..\oleauto\nf-oleauto-safearrayallocdata.md) | Allocates memory for a safe array, based on a descriptor created with SafeArrayAllocDescriptor. |
| [SafeArrayAllocDescriptor function](..\oleauto\nf-oleauto-safearrayallocdescriptor.md) | Allocates memory for a safe array descriptor. |
| [SafeArrayAllocDescriptorEx function](..\oleauto\nf-oleauto-safearrayallocdescriptorex.md) | Creates a safe array descriptor for an array of any valid variant type, including VT_RECORD, without allocating the array data. |
| [SafeArrayCopy function](..\oleauto\nf-oleauto-safearraycopy.md) | Creates a copy of an existing safe array. |
| [SafeArrayCopyData function](..\oleauto\nf-oleauto-safearraycopydata.md) | Copies the source array to the specified target array after releasing any resources in the target array. |
| [SafeArrayCreate function](..\oleauto\nf-oleauto-safearraycreate.md) | Creates a new array descriptor, allocates and initializes the data for the array, and returns a pointer to the new array descriptor. |
| [SafeArrayCreateEx function](..\oleauto\nf-oleauto-safearraycreateex.md) | Creates and returns a safe array descriptor from the specified VARTYPE, number of dimensions and bounds. |
| [SafeArrayCreateVector function](..\oleauto\nf-oleauto-safearraycreatevector.md) | Creates a one-dimensional array. A safe array created with SafeArrayCreateVector is a fixed size, so the constant FADF_FIXEDSIZE is always set. |
| [SafeArrayCreateVectorEx function](..\oleauto\nf-oleauto-safearraycreatevectorex.md) | Creates and returns a one-dimensional safe array of the specified VARTYPE and bounds. |
| [SafeArrayDestroy function](..\oleauto\nf-oleauto-safearraydestroy.md) | Destroys an existing array descriptor and all of the data in the array. |
| [SafeArrayDestroyData function](..\oleauto\nf-oleauto-safearraydestroydata.md) | Destroys all the data in the specified safe array. |
| [SafeArrayDestroyDescriptor function](..\oleauto\nf-oleauto-safearraydestroydescriptor.md) | Destroys the descriptor of the specified safe array. |
| [SafeArrayGetDim function](..\oleauto\nf-oleauto-safearraygetdim.md) | Gets the number of dimensions in the array. |
| [SafeArrayGetElement function](..\oleauto\nf-oleauto-safearraygetelement.md) | Retrieves a single element of the array. |
| [SafeArrayGetElemsize function](..\oleauto\nf-oleauto-safearraygetelemsize.md) | Gets the size of an element. |
| [SafeArrayGetIID function](..\oleauto\nf-oleauto-safearraygetiid.md) | Gets the GUID of the interface contained within the specified safe array. |
| [SafeArrayGetLBound function](..\oleauto\nf-oleauto-safearraygetlbound.md) | Gets the lower bound for any dimension of the specified safe array. |
| [SafeArrayGetRecordInfo function](..\oleauto\nf-oleauto-safearraygetrecordinfo.md) | Retrieves the IRecordInfo interface of the UDT contained in the specified safe array. |
| [SafeArrayGetUBound function](..\oleauto\nf-oleauto-safearraygetubound.md) | Gets the upper bound for any dimension of the specified safe array. |
| [SafeArrayGetVartype function](..\oleauto\nf-oleauto-safearraygetvartype.md) | Gets the VARTYPE stored in the specified safe array. |
| [SafeArrayLock function](..\oleauto\nf-oleauto-safearraylock.md) | Increments the lock count of an array, and places a pointer to the array data in pvData of the array descriptor. |
| [SafeArrayPtrOfIndex function](..\oleauto\nf-oleauto-safearrayptrofindex.md) | Gets a pointer to an array element. |
| [SafeArrayPutElement function](..\oleauto\nf-oleauto-safearrayputelement.md) | Stores the data element at the specified location in the array. |
| [SafeArrayRedim function](..\oleauto\nf-oleauto-safearrayredim.md) | Changes the right-most (least significant) bound of the specified safe array. |
| [SafeArrayReleaseData function](..\oleauto\nf-oleauto-safearrayreleasedata.md) | Decreases the pinning reference count for the specified safe array data by one. When that count reaches 0, the memory for that data is no longer prevented from being freed. |
| [SafeArrayReleaseDescriptor function](..\oleauto\nf-oleauto-safearrayreleasedescriptor.md) | Decreases the pinning reference count for the descriptor of the specified safe array by one. When that count reaches 0, the memory for that descriptor is no longer prevented from being freed. |
| [SafeArraySetIID function](..\oleauto\nf-oleauto-safearraysetiid.md) | Sets the GUID of the interface for the specified safe array. |
| [SafeArraySetRecordInfo function](..\oleauto\nf-oleauto-safearraysetrecordinfo.md) | Sets the record info in the specified safe array. |
| [SafeArrayUnaccessData function](..\oleauto\nf-oleauto-safearrayunaccessdata.md) | Decrements the lock count of an array, and invalidates the pointer retrieved by SafeArrayAccessData. |
| [SafeArrayUnlock function](..\oleauto\nf-oleauto-safearrayunlock.md) | Decrements the lock count of an array so it can be freed or resized. |
| [SetErrorInfo function](..\oleauto\nf-oleauto-seterrorinfo.md) | Sets the error information object for the current logical thread of execution. |
| [SysAddRefString function](..\oleauto\nf-oleauto-sysaddrefstring.md) | Increases the pinning reference count for the specified string by one. |
| [SysAllocString function](..\oleauto\nf-oleauto-sysallocstring.md) | Allocates a new string and copies the passed string into it. |
| [SysAllocStringByteLen function](..\oleauto\nf-oleauto-sysallocstringbytelen.md) | Takes an ANSI string as input, and returns a BSTR that contains an ANSI string. Does not perform any ANSI-to-Unicode translation. |
| [SysAllocStringLen function](..\oleauto\nf-oleauto-sysallocstringlen.md) | Allocates a new string, copies the specified number of characters from the passed string, and appends a null-terminating character. |
| [SysFreeString function](..\oleauto\nf-oleauto-sysfreestring.md) | Deallocates a string allocated previously by SysAllocString, SysAllocStringByteLen, SysReAllocString, SysAllocStringLen, or SysReAllocStringLen. |
| [SysReAllocString function](..\oleauto\nf-oleauto-sysreallocstring.md) | Reallocates a previously allocated string to be the size of a second string and copies the second string into the reallocated memory. |
| [SysReAllocStringLen function](..\oleauto\nf-oleauto-sysreallocstringlen.md) | Creates a new BSTR containing a specified number of characters from an old BSTR, and frees the old BSTR. |
| [SysReleaseString function](..\oleauto\nf-oleauto-sysreleasestring.md) | Decreases the pinning reference count for the specified string by one. When that count reaches 0, the memory for that string is no longer prevented from being freed. |
| [SysStringByteLen function](..\oleauto\nf-oleauto-sysstringbytelen.md) | Returns the length (in bytes) of a BSTR. |
| [SysStringLen function](..\oleauto\nf-oleauto-sysstringlen.md) | Returns the length of a BSTR. |
| [SystemTimeToVariantTime function](..\oleauto\nf-oleauto-systemtimetovarianttime.md) | Converts a system time to a variant representation. |
| [UnRegisterTypeLib function](..\oleauto\nf-oleauto-unregistertypelib.md) | Removes type library information from the system registry. Use this API to allow applications to properly uninstall themselves. |
| [UnRegisterTypeLibForUser function](..\oleauto\nf-oleauto-unregistertypelibforuser.md) | Removes type library information that was registered by using RegisterTypeLibForUser. |
| [VARIANT_UserFree function](..\oaidl\nf-oaidl-variant_userfree.md) | Frees resources on the server side when called by RPC stub files. |
| [VARIANT_UserFree64 function](..\oaidl\nf-oaidl-variant_userfree64.md) | Frees resources on the server side when called by RPC stub files. |
| [VARIANT_UserMarshal function](..\oaidl\nf-oaidl-variant_usermarshal.md) | Marshals a VARIANT object into the RPC buffer. |
| [VARIANT_UserMarshal64 function](..\oaidl\nf-oaidl-variant_usermarshal64.md) | Marshals a VARIANT object into the RPC buffer. |
| [VARIANT_UserSize function](..\oaidl\nf-oaidl-variant_usersize.md) | Calculates the wire size of the VARIANT object, and gets its handle and data. |
| [VARIANT_UserSize64 function](..\oaidl\nf-oaidl-variant_usersize64.md) | Calculates the wire size of the VARIANT object, and gets its handle and data. |
| [VARIANT_UserUnmarshal function](..\oaidl\nf-oaidl-variant_userunmarshal.md) | Unmarshals a VARIANT object from the RPC buffer. |
| [VARIANT_UserUnmarshal64 function](..\oaidl\nf-oaidl-variant_userunmarshal64.md) | Unmarshals a VARIANT object from the RPC buffer. |
| [VarAbs function](..\oleauto\nf-oleauto-varabs.md) | Returns the absolute value of a variant. |
| [VarAdd function](..\oleauto\nf-oleauto-varadd.md) | Returns the sum of two variants. |
| [VarAnd function](..\oleauto\nf-oleauto-varand.md) | Performs a bitwise And operation between two variants of any integral type. |
| [VarBoolFromCy function](..\oleauto\nf-oleauto-varboolfromcy.md) | Converts a currency value to a Boolean value. |
| [VarBoolFromDate function](..\oleauto\nf-oleauto-varboolfromdate.md) | Converts a date value to a Boolean value. |
| [VarBoolFromDec function](..\oleauto\nf-oleauto-varboolfromdec.md) | Converts a decimal value to a Boolean value. |
| [VarBoolFromDisp function](..\oleauto\nf-oleauto-varboolfromdisp.md) | Converts the default property of an IDispatch instance to a Boolean value. |
| [VarBoolFromI1 function](..\oleauto\nf-oleauto-varboolfromi1.md) | Converts a char value to a Boolean value. |
| [VarBoolFromI2 function](..\oleauto\nf-oleauto-varboolfromi2.md) | Converts a short value to a Boolean value. |
| [VarBoolFromI4 function](..\oleauto\nf-oleauto-varboolfromi4.md) | Converts a long value to a Boolean value. |
| [VarBoolFromI8 function](..\oleauto\nf-oleauto-varboolfromi8.md) | Converts an 8-byte integer value to a Boolean value. |
| [VarBoolFromR4 function](..\oleauto\nf-oleauto-varboolfromr4.md) | Converts a float value to a Boolean value. |
| [VarBoolFromR8 function](..\oleauto\nf-oleauto-varboolfromr8.md) | Converts a double value to a Boolean value. |
| [VarBoolFromStr function](..\oleauto\nf-oleauto-varboolfromstr.md) | Converts an OLECHAR string to a Boolean value. |
| [VarBoolFromUI1 function](..\oleauto\nf-oleauto-varboolfromui1.md) | Converts an unsigned char value to a Boolean value. |
| [VarBoolFromUI2 function](..\oleauto\nf-oleauto-varboolfromui2.md) | Converts an unsigned short value to a Boolean value. |
| [VarBoolFromUI4 function](..\oleauto\nf-oleauto-varboolfromui4.md) | Converts an unsigned long value to a Boolean value. |
| [VarBoolFromUI8 function](..\oleauto\nf-oleauto-varboolfromui8.md) | Converts an 8-byte unsigned integer value to a Boolean value. |
| [VarBstrCat function](..\oleauto\nf-oleauto-varbstrcat.md) | Concatenates two variants of type BSTR and returns the resulting BSTR. |
| [VarBstrCmp function](..\oleauto\nf-oleauto-varbstrcmp.md) | Compares two variants of type BSTR. |
| [VarBstrFromBool function](..\oleauto\nf-oleauto-varbstrfrombool.md) | Converts a Boolean value to a BSTR value. |
| [VarBstrFromCy function](..\oleauto\nf-oleauto-varbstrfromcy.md) | Converts a currency value to a BSTR value. |
| [VarBstrFromDate function](..\oleauto\nf-oleauto-varbstrfromdate.md) | Converts a date value to a BSTR value. |
| [VarBstrFromDec function](..\oleauto\nf-oleauto-varbstrfromdec.md) | Converts a decimal value to a BSTR value. |
| [VarBstrFromDisp function](..\oleauto\nf-oleauto-varbstrfromdisp.md) | Converts the default property of an IDispatch instance to a BSTR value. |
| [VarBstrFromI1 function](..\oleauto\nf-oleauto-varbstrfromi1.md) | Converts a char value to a BSTR value. |
| [VarBstrFromI2 function](..\oleauto\nf-oleauto-varbstrfromi2.md) | Converts a short value to a BSTR value. |
| [VarBstrFromI4 function](..\oleauto\nf-oleauto-varbstrfromi4.md) | Converts a long value to a BSTR value. |
| [VarBstrFromI8 function](..\oleauto\nf-oleauto-varbstrfromi8.md) | Converts an 8-byte unsigned integer value to a BSTR value. |
| [VarBstrFromR4 function](..\oleauto\nf-oleauto-varbstrfromr4.md) | Converts a float value to a BSTR value. |
| [VarBstrFromR8 function](..\oleauto\nf-oleauto-varbstrfromr8.md) | Converts a double value to a BSTR value. |
| [VarBstrFromUI1 function](..\oleauto\nf-oleauto-varbstrfromui1.md) | Converts an unsigned char value to a BSTR value. |
| [VarBstrFromUI2 function](..\oleauto\nf-oleauto-varbstrfromui2.md) | Converts an unsigned short value to a BSTR value. |
| [VarBstrFromUI4 function](..\oleauto\nf-oleauto-varbstrfromui4.md) | Converts an unsigned long value to a BSTR value. |
| [VarBstrFromUI8 function](..\oleauto\nf-oleauto-varbstrfromui8.md) | Converts an 8-byte unsigned integer value to a BSTR value. |
| [VarCat function](..\oleauto\nf-oleauto-varcat.md) | Concatenates two variants and returns the result. |
| [VarCmp function](..\oleauto\nf-oleauto-varcmp.md) | Compares two variants. |
| [VarCyAbs function](..\oleauto\nf-oleauto-varcyabs.md) | Retrieves the absolute value of a variant of type currency. |
| [VarCyAdd function](..\oleauto\nf-oleauto-varcyadd.md) | Adds two variants of type currency. |
| [VarCyCmp function](..\oleauto\nf-oleauto-varcycmp.md) | Compares two variants of type currency. |
| [VarCyCmpR8 function](..\oleauto\nf-oleauto-varcycmpr8.md) | Compares a variant of type currency with a value of type double. |
| [VarCyFix function](..\oleauto\nf-oleauto-varcyfix.md) | Retrieves the integer portion of a variant of type currency. |
| [VarCyFromBool function](..\oleauto\nf-oleauto-varcyfrombool.md) | Converts a Boolean value to a currency value. |
| [VarCyFromDate function](..\oleauto\nf-oleauto-varcyfromdate.md) | Converts a date value to a currency value. |
| [VarCyFromDec function](..\oleauto\nf-oleauto-varcyfromdec.md) | Converts a decimal value to a currency value. |
| [VarCyFromDisp function](..\oleauto\nf-oleauto-varcyfromdisp.md) | Converts the default property of an IDispatch instance to a currency value. |
| [VarCyFromI1 function](..\oleauto\nf-oleauto-varcyfromi1.md) | Converts a char value to a currency value. |
| [VarCyFromI2 function](..\oleauto\nf-oleauto-varcyfromi2.md) | Converts a short value to a currency value. |
| [VarCyFromI4 function](..\oleauto\nf-oleauto-varcyfromi4.md) | Converts a long value to a currency value. |
| [VarCyFromI8 function](..\oleauto\nf-oleauto-varcyfromi8.md) | Converts an 8-byte integer value to a currency value. |
| [VarCyFromR4 function](..\oleauto\nf-oleauto-varcyfromr4.md) | Converts a float value to a currency value. |
| [VarCyFromR8 function](..\oleauto\nf-oleauto-varcyfromr8.md) | Converts a double value to a currency value. |
| [VarCyFromStr function](..\oleauto\nf-oleauto-varcyfromstr.md) | Converts an OLECHAR string to a currency value. |
| [VarCyFromUI1 function](..\oleauto\nf-oleauto-varcyfromui1.md) | Converts an unsigned char value to a currency value. |
| [VarCyFromUI2 function](..\oleauto\nf-oleauto-varcyfromui2.md) | Converts an unsigned short value to a currency value. |
| [VarCyFromUI4 function](..\oleauto\nf-oleauto-varcyfromui4.md) | Converts an unsigned long value to a currency value. |
| [VarCyFromUI8 function](..\oleauto\nf-oleauto-varcyfromui8.md) | Converts an 8-byte unsigned integer value to a currency value. |
| [VarCyInt function](..\oleauto\nf-oleauto-varcyint.md) | Retrieves the integer portion of a variant of type currency. |
| [VarCyMul function](..\oleauto\nf-oleauto-varcymul.md) | Multiplies two variants of type currency. |
| [VarCyMulI4 function](..\oleauto\nf-oleauto-varcymuli4.md) | Multiplies a currency value by a 32-bit integer. |
| [VarCyMulI8 function](..\oleauto\nf-oleauto-varcymuli8.md) | Multiplies a currency value by a 64-bit integer. |
| [VarCyNeg function](..\oleauto\nf-oleauto-varcyneg.md) | Performs a logical negation on a variant of type currency. |
| [VarCyRound function](..\oleauto\nf-oleauto-varcyround.md) | Rounds a variant of type currency to the specified number of decimal places. |
| [VarCySub function](..\oleauto\nf-oleauto-varcysub.md) | Subtracts two variants of type currency. |
| [VarDateFromBool function](..\oleauto\nf-oleauto-vardatefrombool.md) | Converts a Boolean value to a date value. |
| [VarDateFromCy function](..\oleauto\nf-oleauto-vardatefromcy.md) | Converts a currency value to a date value. |
| [VarDateFromDec function](..\oleauto\nf-oleauto-vardatefromdec.md) | Converts a decimal value to a date value. |
| [VarDateFromDisp function](..\oleauto\nf-oleauto-vardatefromdisp.md) | Converts the default property of an IDispatch instance to a date value. |
| [VarDateFromI1 function](..\oleauto\nf-oleauto-vardatefromi1.md) | Converts a char value to a date value. |
| [VarDateFromI2 function](..\oleauto\nf-oleauto-vardatefromi2.md) | Converts a short value to a date value. |
| [VarDateFromI4 function](..\oleauto\nf-oleauto-vardatefromi4.md) | Converts a long value to a date value. |
| [VarDateFromI8 function](..\oleauto\nf-oleauto-vardatefromi8.md) | Converts an 8-byte unsigned integer value to a date value. |
| [VarDateFromR4 function](..\oleauto\nf-oleauto-vardatefromr4.md) | Converts a float value to a date value. |
| [VarDateFromR8 function](..\oleauto\nf-oleauto-vardatefromr8.md) | Converts a double value to a date value. |
| [VarDateFromStr function](..\oleauto\nf-oleauto-vardatefromstr.md) | Converts an OLECHAR string to a date value. |
| [VarDateFromUI1 function](..\oleauto\nf-oleauto-vardatefromui1.md) | Converts an unsigned char value to a date value. |
| [VarDateFromUI2 function](..\oleauto\nf-oleauto-vardatefromui2.md) | Converts an unsigned short value to a date value. |
| [VarDateFromUI4 function](..\oleauto\nf-oleauto-vardatefromui4.md) | Converts an unsigned long value to a date value. |
| [VarDateFromUI8 function](..\oleauto\nf-oleauto-vardatefromui8.md) | Converts an 8-byte unsigned value to a date value. |
| [VarDateFromUdate function](..\oleauto\nf-oleauto-vardatefromudate.md) | Converts a time and date converted from MS-DOS format to variant format. |
| [VarDateFromUdateEx function](..\oleauto\nf-oleauto-vardatefromudateex.md) | Converts a time and date converted from MS-DOS format to variant format. |
| [VarDecAbs function](..\oleauto\nf-oleauto-vardecabs.md) | Retrieves the absolute value of a variant of type decimal. |
| [VarDecAdd function](..\oleauto\nf-oleauto-vardecadd.md) | Adds two variants of type decimal. |
| [VarDecCmp function](..\oleauto\nf-oleauto-vardeccmp.md) | Compares two variants of type decimal. |
| [VarDecCmpR8 function](..\oleauto\nf-oleauto-vardeccmpr8.md) | Compares a variant of type decimal with the a value of type double. |
| [VarDecDiv function](..\oleauto\nf-oleauto-vardecdiv.md) | Divides two variants of type decimal. |
| [VarDecFix function](..\oleauto\nf-oleauto-vardecfix.md) | Retrieves the integer portion of a variant of type decimal. |
| [VarDecFromBool function](..\oleauto\nf-oleauto-vardecfrombool.md) | Converts a Boolean value to a decimal value. |
| [VarDecFromCy function](..\oleauto\nf-oleauto-vardecfromcy.md) | Converts a currency value to a decimal value. |
| [VarDecFromDate function](..\oleauto\nf-oleauto-vardecfromdate.md) | Converts a date value to a decimal value. |
| [VarDecFromDisp function](..\oleauto\nf-oleauto-vardecfromdisp.md) | Converts the default property of an IDispatch instance to a decimal value. |
| [VarDecFromI1 function](..\oleauto\nf-oleauto-vardecfromi1.md) | Converts a char value to a decimal value. |
| [VarDecFromI2 function](..\oleauto\nf-oleauto-vardecfromi2.md) | Converts a short value to a decimal value. |
| [VarDecFromI4 function](..\oleauto\nf-oleauto-vardecfromi4.md) | Converts a long value to a decimal value. |
| [VarDecFromI8 function](..\oleauto\nf-oleauto-vardecfromi8.md) | Converts an 8-byte integer value to a decimal value. |
| [VarDecFromR4 function](..\oleauto\nf-oleauto-vardecfromr4.md) | Converts a float value to a decimal value. |
| [VarDecFromR8 function](..\oleauto\nf-oleauto-vardecfromr8.md) | Converts a double value to a decimal value. |
| [VarDecFromStr function](..\oleauto\nf-oleauto-vardecfromstr.md) | Converts an OLECHAR string to a decimal value. |
| [VarDecFromUI1 function](..\oleauto\nf-oleauto-vardecfromui1.md) | Converts an unsigned char value to a decimal value. |
| [VarDecFromUI2 function](..\oleauto\nf-oleauto-vardecfromui2.md) | Converts an unsigned short value to a decimal value. |
| [VarDecFromUI4 function](..\oleauto\nf-oleauto-vardecfromui4.md) | Converts an unsigned long value to a decimal value. |
| [VarDecFromUI8 function](..\oleauto\nf-oleauto-vardecfromui8.md) | Converts an 8-byte unsigned integer value to a decimal value. |
| [VarDecInt function](..\oleauto\nf-oleauto-vardecint.md) | Retrieves the integer portion of a variant of type decimal. |
| [VarDecMul function](..\oleauto\nf-oleauto-vardecmul.md) | Multiplies two variants of type decimal. |
| [VarDecNeg function](..\oleauto\nf-oleauto-vardecneg.md) | Performs logical negation on a variant of type decimal. |
| [VarDecRound function](..\oleauto\nf-oleauto-vardecround.md) | Rounds a variant of type decimal to the specified number of decimal places. |
| [VarDecSub function](..\oleauto\nf-oleauto-vardecsub.md) | Subtracts two variants of type decimal. |
| [VarDiv function](..\oleauto\nf-oleauto-vardiv.md) | Returns the result from dividing two variants. |
| [VarEqv function](..\oleauto\nf-oleauto-vareqv.md) | Performs a bitwise equivalence on two variants. |
| [VarFix function](..\oleauto\nf-oleauto-varfix.md) | Returns the integer portion of a variant. |
| [VarFormat function](..\oleauto\nf-oleauto-varformat.md) | Formats a variant into string form by parsing a format string. |
| [VarFormatCurrency function](..\oleauto\nf-oleauto-varformatcurrency.md) | Formats a variant containing currency values into a string form. |
| [VarFormatDateTime function](..\oleauto\nf-oleauto-varformatdatetime.md) | Formats a variant containing named date and time information into a string. |
| [VarFormatFromTokens function](..\oleauto\nf-oleauto-varformatfromtokens.md) | Takes a tokenized format string and applies it to a variant to produce a formatted output string. |
| [VarFormatNumber function](..\oleauto\nf-oleauto-varformatnumber.md) | Formats a variant containing numbers into a string form. |
| [VarFormatPercent function](..\oleauto\nf-oleauto-varformatpercent.md) | Formats a variant containing percentages into a string form. |
| [VarI1FromBool function](..\oleauto\nf-oleauto-vari1frombool.md) | Converts a Boolean value to a char value. |
| [VarI1FromCy function](..\oleauto\nf-oleauto-vari1fromcy.md) | Converts a currency value to a char value. |
| [VarI1FromDate function](..\oleauto\nf-oleauto-vari1fromdate.md) | Converts a date value to a char value. |
| [VarI1FromDec function](..\oleauto\nf-oleauto-vari1fromdec.md) | Converts a decimal value to a char value. |
| [VarI1FromDisp function](..\oleauto\nf-oleauto-vari1fromdisp.md) | Converts the default property of an IDispatch instance to a char value. |
| [VarI1FromI2 function](..\oleauto\nf-oleauto-vari1fromi2.md) | Converts a short value to a char value. |
| [VarI1FromI4 function](..\oleauto\nf-oleauto-vari1fromi4.md) | Converts a long value to a char value. |
| [VarI1FromI8 function](..\oleauto\nf-oleauto-vari1fromi8.md) | Converts an 8-byte integer value to a char value. |
| [VarI1FromR4 function](..\oleauto\nf-oleauto-vari1fromr4.md) | Converts a float value to a char value. |
| [VarI1FromR8 function](..\oleauto\nf-oleauto-vari1fromr8.md) | Converts a double value to a char value. |
| [VarI1FromStr function](..\oleauto\nf-oleauto-vari1fromstr.md) | Converts an OLECHAR string to a char value. |
| [VarI1FromUI1 function](..\oleauto\nf-oleauto-vari1fromui1.md) | Converts an unsigned char value to a char value. |
| [VarI1FromUI2 function](..\oleauto\nf-oleauto-vari1fromui2.md) | Converts an unsigned short value to a char value. |
| [VarI1FromUI4 function](..\oleauto\nf-oleauto-vari1fromui4.md) | Converts an unsigned long value to a char value. |
| [VarI1FromUI8 function](..\oleauto\nf-oleauto-vari1fromui8.md) | Converts an 8-byte unsigned integer value to a char value. |
| [VarI2FromBool function](..\oleauto\nf-oleauto-vari2frombool.md) | Converts a Boolean value to a short value. |
| [VarI2FromCy function](..\oleauto\nf-oleauto-vari2fromcy.md) | Converts a currency value to a short value. |
| [VarI2FromDate function](..\oleauto\nf-oleauto-vari2fromdate.md) | Converts a date value to a short value. |
| [VarI2FromDec function](..\oleauto\nf-oleauto-vari2fromdec.md) | Converts a decimal value to a short value. |
| [VarI2FromDisp function](..\oleauto\nf-oleauto-vari2fromdisp.md) | Converts the default property of an IDispatch instance to a short value. |
| [VarI2FromI1 function](..\oleauto\nf-oleauto-vari2fromi1.md) | Converts a char value to a short value. |
| [VarI2FromI4 function](..\oleauto\nf-oleauto-vari2fromi4.md) | Converts a long value to a short value. |
| [VarI2FromI8 function](..\oleauto\nf-oleauto-vari2fromi8.md) | Converts an 8-byte integer value to a short value. |
| [VarI2FromR4 function](..\oleauto\nf-oleauto-vari2fromr4.md) | Converts a float value to a short value. |
| [VarI2FromR8 function](..\oleauto\nf-oleauto-vari2fromr8.md) | Converts a double value to a short value. |
| [VarI2FromStr function](..\oleauto\nf-oleauto-vari2fromstr.md) | Converts an OLECHAR string to a short value. |
| [VarI2FromUI1 function](..\oleauto\nf-oleauto-vari2fromui1.md) | Converts an unsigned char value to a short value. |
| [VarI2FromUI2 function](..\oleauto\nf-oleauto-vari2fromui2.md) | Converts an unsigned short value to a short value. |
| [VarI2FromUI4 function](..\oleauto\nf-oleauto-vari2fromui4.md) | Converts an unsigned long value to a short value. |
| [VarI2FromUI8 function](..\oleauto\nf-oleauto-vari2fromui8.md) | Converts an 8-byte unsigned integer value to a short value. |
| [VarI4FromBool function](..\oleauto\nf-oleauto-vari4frombool.md) | Converts a Boolean value to a long value. |
| [VarI4FromCy function](..\oleauto\nf-oleauto-vari4fromcy.md) | Converts a currency value to a long value. |
| [VarI4FromDate function](..\oleauto\nf-oleauto-vari4fromdate.md) | Converts a date value to a long value. |
| [VarI4FromDec function](..\oleauto\nf-oleauto-vari4fromdec.md) | Converts a decimal value to a long value. |
| [VarI4FromDisp function](..\oleauto\nf-oleauto-vari4fromdisp.md) | Converts the default property of an IDispatch instance to a long value. |
| [VarI4FromI1 function](..\oleauto\nf-oleauto-vari4fromi1.md) | Converts a char value to a long value. |
| [VarI4FromI2 function](..\oleauto\nf-oleauto-vari4fromi2.md) | Converts a short value to a long value. |
| [VarI4FromI8 function](..\oleauto\nf-oleauto-vari4fromi8.md) | Converts an 8-byte integer value to a long value. |
| [VarI4FromR4 function](..\oleauto\nf-oleauto-vari4fromr4.md) | Converts a float value to a long value. |
| [VarI4FromR8 function](..\oleauto\nf-oleauto-vari4fromr8.md) | Converts a double value to a long value. |
| [VarI4FromStr function](..\oleauto\nf-oleauto-vari4fromstr.md) | Converts an OLECHAR string to a long value. |
| [VarI4FromUI1 function](..\oleauto\nf-oleauto-vari4fromui1.md) | Converts an unsigned char value to a long value. |
| [VarI4FromUI2 function](..\oleauto\nf-oleauto-vari4fromui2.md) | Converts an unsigned short value to a long value. |
| [VarI4FromUI4 function](..\oleauto\nf-oleauto-vari4fromui4.md) | Converts an unsigned long value to a long value. |
| [VarI4FromUI8 function](..\oleauto\nf-oleauto-vari4fromui8.md) | Converts an 8-byte unsigned integer value to a long. |
| [VarI8FromBool function](..\oleauto\nf-oleauto-vari8frombool.md) | Converts a Boolean value to an 8-byte integer value. |
| [VarI8FromCy function](..\oleauto\nf-oleauto-vari8fromcy.md) | Converts a currency value to an 8-byte integer value. |
| [VarI8FromDate function](..\oleauto\nf-oleauto-vari8fromdate.md) | Converts a date value to an 8-byte integer value. |
| [VarI8FromDec function](..\oleauto\nf-oleauto-vari8fromdec.md) | Converts a decimal value to an 8-byte integer value. |
| [VarI8FromDisp function](..\oleauto\nf-oleauto-vari8fromdisp.md) | Converts the default property of an IDispatch instance to an 8-byte integer value. |
| [VarI8FromI1 function](..\oleauto\nf-oleauto-vari8fromi1.md) | Converts a char value to an 8-byte integer value. |
| [VarI8FromI2 function](..\oleauto\nf-oleauto-vari8fromi2.md) | Converts a short value to an 8-byte integer value. |
| [VarI8FromR4 function](..\oleauto\nf-oleauto-vari8fromr4.md) | Converts a float value to an 8-byte integer value. |
| [VarI8FromR8 function](..\oleauto\nf-oleauto-vari8fromr8.md) | Converts a double value to an 8-byte integer value. |
| [VarI8FromStr function](..\oleauto\nf-oleauto-vari8fromstr.md) | Converts an OLECHAR string to an 8-byte integer value. |
| [VarI8FromUI1 function](..\oleauto\nf-oleauto-vari8fromui1.md) | Onverts an unsigned byte value to an 8-byte integer value. |
| [VarI8FromUI2 function](..\oleauto\nf-oleauto-vari8fromui2.md) | Converts an unsigned short value to an 8-byte integer value. |
| [VarI8FromUI4 function](..\oleauto\nf-oleauto-vari8fromui4.md) | Converts an unsigned long value to an 8-byte integer value. |
| [VarI8FromUI8 function](..\oleauto\nf-oleauto-vari8fromui8.md) | Converts an unsigned 8-byte integer value to an 8-byte integer value. |
| [VarIdiv function](..\oleauto\nf-oleauto-varidiv.md) | Converts two variants of any type to integers then returns the result from dividing them. |
| [VarImp function](..\oleauto\nf-oleauto-varimp.md) | Performs a bitwise implication on two variants. |
| [VarInt function](..\oleauto\nf-oleauto-varint.md) | Returns the integer portion of a variant. |
| [VarMod function](..\oleauto\nf-oleauto-varmod.md) | Divides two variants and returns only the remainder. |
| [VarMonthName function](..\oleauto\nf-oleauto-varmonthname.md) | Returns a string containing the localized month name. |
| [VarMul function](..\oleauto\nf-oleauto-varmul.md) | Returns the result from multiplying two variants. |
| [VarNeg function](..\oleauto\nf-oleauto-varneg.md) | Performs logical negation on a variant. |
| [VarNot function](..\oleauto\nf-oleauto-varnot.md) | Performs the bitwise not negation operation on a variant. |
| [VarNumFromParseNum function](..\oleauto\nf-oleauto-varnumfromparsenum.md) | Converts parsed results to a variant. |
| [VarOr function](..\oleauto\nf-oleauto-varor.md) | Performs a logical disjunction on two variants. |
| [VarParseNumFromStr function](..\oleauto\nf-oleauto-varparsenumfromstr.md) | Parses a string, and creates a type-independent description of the number it represents. |
| [VarPow function](..\oleauto\nf-oleauto-varpow.md) | Returns the result of performing the power function with two variants. |
| [VarR4CmpR8 function](..\oleauto\nf-oleauto-varr4cmpr8.md) | Compares two variants of types float and double. |
| [VarR4FromBool function](..\oleauto\nf-oleauto-varr4frombool.md) | Converts a Boolean value to a float value. |
| [VarR4FromCy function](..\oleauto\nf-oleauto-varr4fromcy.md) | Converts a currency value to a float value. |
| [VarR4FromDate function](..\oleauto\nf-oleauto-varr4fromdate.md) | Converts a date value to a float value. |
| [VarR4FromDec function](..\oleauto\nf-oleauto-varr4fromdec.md) | Converts a decimal value to a float value. |
| [VarR4FromDisp function](..\oleauto\nf-oleauto-varr4fromdisp.md) | Converts the default property of an IDispatch instance to a float value. |
| [VarR4FromI1 function](..\oleauto\nf-oleauto-varr4fromi1.md) | Onverts a char value to a float value. |
| [VarR4FromI2 function](..\oleauto\nf-oleauto-varr4fromi2.md) | Converts a short value to a float value. |
| [VarR4FromI4 function](..\oleauto\nf-oleauto-varr4fromi4.md) | Converts a long value to a float value. |
| [VarR4FromI8 function](..\oleauto\nf-oleauto-varr4fromi8.md) | Converts an 8-byte integer value to a float value. |
| [VarR4FromR8 function](..\oleauto\nf-oleauto-varr4fromr8.md) | Converts a double value to a float value. |
| [VarR4FromStr function](..\oleauto\nf-oleauto-varr4fromstr.md) | Converts an OLECHAR string to a float value. |
| [VarR4FromUI1 function](..\oleauto\nf-oleauto-varr4fromui1.md) | Converts an unsigned char value to a float value. |
| [VarR4FromUI2 function](..\oleauto\nf-oleauto-varr4fromui2.md) | Converts an unsigned short value to a float value. |
| [VarR4FromUI4 function](..\oleauto\nf-oleauto-varr4fromui4.md) | Converts an unsigned long value to a float value. |
| [VarR4FromUI8 function](..\oleauto\nf-oleauto-varr4fromui8.md) | Converts an unsigned 8-byte integer value to a float value. |
| [VarR8FromBool function](..\oleauto\nf-oleauto-varr8frombool.md) | Converts a Boolean value to a double value. |
| [VarR8FromCy function](..\oleauto\nf-oleauto-varr8fromcy.md) | Converts a currency value to a double value. |
| [VarR8FromDate function](..\oleauto\nf-oleauto-varr8fromdate.md) | Converts a date value to a double value. |
| [VarR8FromDec function](..\oleauto\nf-oleauto-varr8fromdec.md) | Converts a decimal value to a double value. |
| [VarR8FromDisp function](..\oleauto\nf-oleauto-varr8fromdisp.md) | Converts the default property of an IDispatch instance to a double value. |
| [VarR8FromI1 function](..\oleauto\nf-oleauto-varr8fromi1.md) | Converts a char value to a double value. |
| [VarR8FromI2 function](..\oleauto\nf-oleauto-varr8fromi2.md) | Converts a short value to a double value. |
| [VarR8FromI4 function](..\oleauto\nf-oleauto-varr8fromi4.md) | Converts a long value to a double value. |
| [VarR8FromI8 function](..\oleauto\nf-oleauto-varr8fromi8.md) | Converts an 8-byte integer value to a double value. |
| [VarR8FromR4 function](..\oleauto\nf-oleauto-varr8fromr4.md) | Converts a float value to a double value. |
| [VarR8FromStr function](..\oleauto\nf-oleauto-varr8fromstr.md) | Converts an OLECHAR string to a double value. |
| [VarR8FromUI1 function](..\oleauto\nf-oleauto-varr8fromui1.md) | Converts an unsigned char value to a double value. |
| [VarR8FromUI2 function](..\oleauto\nf-oleauto-varr8fromui2.md) | Converts an unsigned short value to a double value. |
| [VarR8FromUI4 function](..\oleauto\nf-oleauto-varr8fromui4.md) | Converts an unsigned long value to a double value. |
| [VarR8FromUI8 function](..\oleauto\nf-oleauto-varr8fromui8.md) | Converts an 8-byte unsigned integer value to a double value. |
| [VarR8Pow function](..\oleauto\nf-oleauto-varr8pow.md) | Performs the power function for variants of type double. |
| [VarR8Round function](..\oleauto\nf-oleauto-varr8round.md) | Rounds a variant of type double to the specified number of decimal places. |
| [VarRound function](..\oleauto\nf-oleauto-varround.md) | Rounds a variant to the specified number of decimal places. |
| [VarSub function](..\oleauto\nf-oleauto-varsub.md) | Subtracts two variants. |
| [VarTokenizeFormatString function](..\oleauto\nf-oleauto-vartokenizeformatstring.md) | Parses the actual format string into a series of tokens which can be used to format variants using VarFormatFromTokens. |
| [VarUI1FromBool function](..\oleauto\nf-oleauto-varui1frombool.md) | Converts a Boolean value to an unsigned char value. |
| [VarUI1FromCy function](..\oleauto\nf-oleauto-varui1fromcy.md) | Converts a currency value to an unsigned char value. |
| [VarUI1FromDate function](..\oleauto\nf-oleauto-varui1fromdate.md) | Converts a date value to an unsigned char value. |
| [VarUI1FromDec function](..\oleauto\nf-oleauto-varui1fromdec.md) | Converts a decimal value to an unsigned char value. |
| [VarUI1FromDisp function](..\oleauto\nf-oleauto-varui1fromdisp.md) | Converts the default property of an IDispatch instance to an unsigned char value. |
| [VarUI1FromI1 function](..\oleauto\nf-oleauto-varui1fromi1.md) | Converts a char value to an unsigned char value. |
| [VarUI1FromI2 function](..\oleauto\nf-oleauto-varui1fromi2.md) | Converts a short value to an unsigned char value. |
| [VarUI1FromI4 function](..\oleauto\nf-oleauto-varui1fromi4.md) | Converts a long value to an unsigned char value. |
| [VarUI1FromI8 function](..\oleauto\nf-oleauto-varui1fromi8.md) | Converts an 8-byte integer value to a byte value. |
| [VarUI1FromR4 function](..\oleauto\nf-oleauto-varui1fromr4.md) | Converts a float value to an unsigned char value. |
| [VarUI1FromR8 function](..\oleauto\nf-oleauto-varui1fromr8.md) | Converts a double value to an unsigned char value. |
| [VarUI1FromStr function](..\oleauto\nf-oleauto-varui1fromstr.md) | Converts an OLECHAR string to an unsigned char string. |
| [VarUI1FromUI2 function](..\oleauto\nf-oleauto-varui1fromui2.md) | Converts an unsigned short value to an unsigned char value. |
| [VarUI1FromUI4 function](..\oleauto\nf-oleauto-varui1fromui4.md) | Converts an unsigned long value to an unsigned char value. |
| [VarUI1FromUI8 function](..\oleauto\nf-oleauto-varui1fromui8.md) | Converts an 8-byte unsigned integer value to a byte value. |
| [VarUI2FromBool function](..\oleauto\nf-oleauto-varui2frombool.md) | Converts a Boolean value to an unsigned short value. |
| [VarUI2FromCy function](..\oleauto\nf-oleauto-varui2fromcy.md) | Converts a currency value to an unsigned short value. |
| [VarUI2FromDate function](..\oleauto\nf-oleauto-varui2fromdate.md) | Converts a date value to an unsigned short value. |
| [VarUI2FromDec function](..\oleauto\nf-oleauto-varui2fromdec.md) | Converts a decimal value to an unsigned short value. |
| [VarUI2FromDisp function](..\oleauto\nf-oleauto-varui2fromdisp.md) | Converts the default property of an IDispatch instance to an unsigned short value. |
| [VarUI2FromI1 function](..\oleauto\nf-oleauto-varui2fromi1.md) | Converts a char value to an unsigned short value. |
| [VarUI2FromI2 function](..\oleauto\nf-oleauto-varui2fromi2.md) | Converts a short value to an unsigned short value. |
| [VarUI2FromI4 function](..\oleauto\nf-oleauto-varui2fromi4.md) | Converts a long value to an unsigned short value. |
| [VarUI2FromI8 function](..\oleauto\nf-oleauto-varui2fromi8.md) | Converts an 8-byte integer value to an unsigned short value. |
| [VarUI2FromR4 function](..\oleauto\nf-oleauto-varui2fromr4.md) | Converts a float value to an unsigned short value. |
| [VarUI2FromR8 function](..\oleauto\nf-oleauto-varui2fromr8.md) | Converts a double value to an unsigned short value. |
| [VarUI2FromStr function](..\oleauto\nf-oleauto-varui2fromstr.md) | Converts an OLECHAR string to an unsigned short value. |
| [VarUI2FromUI1 function](..\oleauto\nf-oleauto-varui2fromui1.md) | Converts an unsigned char value to an unsigned short value. |
| [VarUI2FromUI4 function](..\oleauto\nf-oleauto-varui2fromui4.md) | Converts an unsigned long value to an unsigned short value. |
| [VarUI2FromUI8 function](..\oleauto\nf-oleauto-varui2fromui8.md) | Converts an 8-byte unsigned integer value to an unsigned short value. |
| [VarUI4FromBool function](..\oleauto\nf-oleauto-varui4frombool.md) | Converts a Boolean value to an unsigned long value. |
| [VarUI4FromCy function](..\oleauto\nf-oleauto-varui4fromcy.md) | Converts a currency value to an unsigned long value. |
| [VarUI4FromDate function](..\oleauto\nf-oleauto-varui4fromdate.md) | Converts a date value to an unsigned long value. |
| [VarUI4FromDec function](..\oleauto\nf-oleauto-varui4fromdec.md) | Converts a decimal value to an unsigned long value. |
| [VarUI4FromDisp function](..\oleauto\nf-oleauto-varui4fromdisp.md) | Converts the default property of an IDispatch instance to an unsigned long value. |
| [VarUI4FromI1 function](..\oleauto\nf-oleauto-varui4fromi1.md) | Converts a char value to an unsigned long value. |
| [VarUI4FromI2 function](..\oleauto\nf-oleauto-varui4fromi2.md) | Converts a short value to an unsigned long value. |
| [VarUI4FromI4 function](..\oleauto\nf-oleauto-varui4fromi4.md) | Converts a long value to an unsigned long value. |
| [VarUI4FromI8 function](..\oleauto\nf-oleauto-varui4fromi8.md) | Converts an 8-byte integer value to an unsigned long value. |
| [VarUI4FromR4 function](..\oleauto\nf-oleauto-varui4fromr4.md) | Converts a float value to an unsigned long value. |
| [VarUI4FromR8 function](..\oleauto\nf-oleauto-varui4fromr8.md) | Converts a double value to an unsigned long value. |
| [VarUI4FromStr function](..\oleauto\nf-oleauto-varui4fromstr.md) | Converts an OLECHAR string to an unsigned long value. |
| [VarUI4FromUI1 function](..\oleauto\nf-oleauto-varui4fromui1.md) | Converts an unsigned char value to an unsigned long value. |
| [VarUI4FromUI2 function](..\oleauto\nf-oleauto-varui4fromui2.md) | Converts an unsigned short value to an unsigned long value. |
| [VarUI4FromUI8 function](..\oleauto\nf-oleauto-varui4fromui8.md) | Converts an 8-byte unsigned integer value to an unsigned long value. |
| [VarUI8FromBool function](..\oleauto\nf-oleauto-varui8frombool.md) | Converts a VARIANT_BOOL value to an 8-byte unsigned integer value. |
| [VarUI8FromCy function](..\oleauto\nf-oleauto-varui8fromcy.md) | Converts a currency value to an 8-byte unsigned integer value. |
| [VarUI8FromDate function](..\oleauto\nf-oleauto-varui8fromdate.md) | Converts a date value to an 8-byte unsigned integer value. |
| [VarUI8FromDec function](..\oleauto\nf-oleauto-varui8fromdec.md) | Converts a decimal value to an 8-byte unsigned integer value. |
| [VarUI8FromDisp function](..\oleauto\nf-oleauto-varui8fromdisp.md) | Converts the default property of an IDispatch instance to an 8-byte unsigned integer value. |
| [VarUI8FromI1 function](..\oleauto\nf-oleauto-varui8fromi1.md) | Converts a char value to an 8-byte unsigned integer value. |
| [VarUI8FromI2 function](..\oleauto\nf-oleauto-varui8fromi2.md) | Converts a short value to an 8-byte unsigned integer value. |
| [VarUI8FromI8 function](..\oleauto\nf-oleauto-varui8fromi8.md) | Converts an 8-byte integer value to an 8-byte unsigned integer value. |
| [VarUI8FromR4 function](..\oleauto\nf-oleauto-varui8fromr4.md) | Converts a float value to an 8-byte unsigned integer value. |
| [VarUI8FromR8 function](..\oleauto\nf-oleauto-varui8fromr8.md) | Converts a double value to an 8-byte unsigned integer value. |
| [VarUI8FromStr function](..\oleauto\nf-oleauto-varui8fromstr.md) | Converts an OLECHAR string to an 8-byte unsigned integer value. |
| [VarUI8FromUI1 function](..\oleauto\nf-oleauto-varui8fromui1.md) | Converts a byte value to an 8-byte unsigned integer value. |
| [VarUI8FromUI2 function](..\oleauto\nf-oleauto-varui8fromui2.md) | Converts an unsigned short value to an 8-byte unsigned integer value. |
| [VarUI8FromUI4 function](..\oleauto\nf-oleauto-varui8fromui4.md) | Converts an unsigned long value to an 8-byte unsigned integer value. |
| [VarUdateFromDate function](..\oleauto\nf-oleauto-varudatefromdate.md) | Converts a time and date converted from variant format to MS-DOS format. |
| [VarWeekdayName function](..\oleauto\nf-oleauto-varweekdayname.md) | Returns a string containing the localized name of the weekday. |
| [VarXor function](..\oleauto\nf-oleauto-varxor.md) | Performs a logical exclusion on two variants. |
| [VariantChangeType function](..\oleauto\nf-oleauto-variantchangetype.md) | Converts a variant from one type to another. |
| [VariantChangeTypeEx function](..\oleauto\nf-oleauto-variantchangetypeex.md) | Converts a variant from one type to another, using an LCID. |
| [VariantClear function](..\oleauto\nf-oleauto-variantclear.md) | Clears a variant. |
| [VariantCopy function](..\oleauto\nf-oleauto-variantcopy.md) | Frees the destination variant and makes a copy of the source variant. |
| [VariantCopyInd function](..\oleauto\nf-oleauto-variantcopyind.md) | Frees the destination variant and makes a copy of the source variant, performing the necessary indirection if the source is specified to be VT_BYREF. |
| [VariantInit function](..\oleauto\nf-oleauto-variantinit.md) | Initializes a variant. |
| [VariantTimeToDosDateTime function](..\oleauto\nf-oleauto-varianttimetodosdatetime.md) | Converts the variant representation of a date and time to MS-DOS date and time values. |
| [VariantTimeToSystemTime function](..\oleauto\nf-oleauto-varianttimetosystemtime.md) | Converts the variant representation of time to system time values. |
| [VectorFromBstr function](..\oleauto\nf-oleauto-vectorfrombstr.md) | Returns a vector, assigning each character in the BSTR to an element of the vector. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [NUMPARSE structure](..\oleauto\ns-oleauto-numparse.md) | Specifies numeric parsing information. |
| [tagARRAYDESC structure](..\oaidl\ns-oaidl-tagarraydesc.md) | Describes an array, its element type, and its dimension. |
| [tagBINDPTR structure](..\oaidl\ns-oaidl-tagbindptr.md) | Describes a pointer. |
| [tagCUSTDATA structure](..\oaidl\ns-oaidl-tagcustdata.md) | Represents custom data. |
| [tagCUSTDATAITEM structure](..\oaidl\ns-oaidl-tagcustdataitem.md) | Represents a custom data item. |
| [tagDISPPARAMS structure](..\oaidl\ns-oaidl-tagdispparams.md) | Contains the arguments passed to a method or property. |
| [tagELEMDESC structure](..\oaidl\ns-oaidl-tagelemdesc.md) | Contains the type description and process-transfer information for a variable, a function, or a function parameter. |
| [tagEXCEPINFO structure](..\oaidl\ns-oaidl-tagexcepinfo.md) | Describes an exception that occurred during IDispatch |
| [tagFUNCDESC structure](..\oaidl\ns-oaidl-tagfuncdesc.md) | Describes a function. |
| [tagINTERFACEDATA structure](..\oleauto\ns-oleauto-taginterfacedata.md) | Describes the object's properties and methods. |
| [tagMETHODDATA structure](..\oleauto\ns-oleauto-tagmethoddata.md) | Describes a method or property. |
| [tagPARAMDATA structure](..\oleauto\ns-oleauto-tagparamdata.md) | Describes a parameter accepted by a method or property. |
| [tagPARAMDESC structure](..\oaidl\ns-oaidl-tagparamdesc.md) | Contains information needed for transferring a structure element, parameter, or function return value between processes. |
| [tagPARAMDESCEX structure](..\oaidl\ns-oaidl-tagparamdescex.md) | Contains information about the default value of a parameter. |
| [tagSAFEARRAY structure](..\oaidl\ns-oaidl-tagsafearray.md) | Represents a safe array. |
| [tagSAFEARRAYBOUND structure](..\oaidl\ns-oaidl-tagsafearraybound.md) | Represents the bounds of one dimension of the array. |
| [tagTLIBATTR structure](..\oaidl\ns-oaidl-tagtlibattr.md) | Contains information about a type library. Information from this structure is used to identify the type library and to provide national language support for member names. |
| [tagTYPEATTR structure](..\oaidl\ns-oaidl-tagtypeattr.md) | Contains attributes of a type. |
| [tagTYPEDESC structure](..\oaidl\ns-oaidl-tagtypedesc.md) | Describes the type of a variable, the return type of a function, or the type of a function parameter. |
| [tagVARDESC structure](..\oaidl\ns-oaidl-tagvardesc.md) | Describes a variable, constant, or data member. |
| [tagVARIANT structure](..\oaidl\ns-oaidl-tagvariant.md) | VARIANTARG describes arguments passed within DISPPARAMS, and VARIANT to specify variant data that cannot be passed by reference. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [VARENUM enumeration](..\wtypes\ne-wtypes-varenum.md) | Specifies the variant types. |
| [tagCALLCONV enumeration](..\oaidl\ne-oaidl-tagcallconv.md) | Identifies the calling convention used by a member function described in the METHODDATA structure. |
| [tagDESCKIND enumeration](..\oaidl\ne-oaidl-tagdesckind.md) | Identifies the type description being bound to. |
| [tagFUNCFLAGS enumeration](..\oaidl\ne-oaidl-tagfuncflags.md) | Specifies function flags. |
| [tagFUNCKIND enumeration](..\oaidl\ne-oaidl-tagfunckind.md) | Specifies the function type. |
| [tagINVOKEKIND enumeration](..\oaidl\ne-oaidl-taginvokekind.md) | Specifies the way a function is invoked. |
| [tagLIBFLAGS enumeration](..\oaidl\ne-oaidl-taglibflags.md) | Defines flags that apply to type libraries. |
| [tagREGKIND enumeration](..\oleauto\ne-oleauto-tagregkind.md) | Controls how a type library is registered. |
| [tagSYSKIND enumeration](..\oaidl\ne-oaidl-tagsyskind.md) | Identifies the target operating system platform. |
| [tagTYPEFLAGS enumeration](..\oaidl\ne-oaidl-tagtypeflags.md) | The type flags. |
| [tagTYPEKIND enumeration](..\oaidl\ne-oaidl-tagtypekind.md) | Specifies a type. |
| [tagVARFLAGS enumeration](..\oaidl\ne-oaidl-tagvarflags.md) | Specifies variable flags. |
| [tagVARKIND enumeration](..\oaidl\ne-oaidl-tagvarkind.md) | Specifies the variable type. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [ICreateErrorInfo interface](..\oaidl\nn-oaidl-icreateerrorinfo.md) | Returns error information. |
| [ICreateTypeInfo interface](..\oaidl\nn-oaidl-icreatetypeinfo.md) | Provides the tools for creating and administering the type information defined through the type description. |
| [ICreateTypeInfo2 interface](..\oaidl\nn-oaidl-icreatetypeinfo2.md) | Provides the tools for creating and administering the type information defined through the type description. |
| [ICreateTypeLib interface](..\oaidl\nn-oaidl-icreatetypelib.md) | Provides the methods for creating and managing the component or file that contains type information. |
| [ICreateTypeLib2 interface](..\oaidl\nn-oaidl-icreatetypelib2.md) | Provides the methods for creating and managing the component or file that contains type information. |
| [IDispatch interface](..\oaidl\nn-oaidl-idispatch.md) | Exposes objects, methods and properties to programming tools and other applications that support Automation. |
| [IEnumVARIANT interface](..\oaidl\nn-oaidl-ienumvariant.md) | Provides a method for enumerating a collection of variants, including heterogeneous collections of objects and intrinsic types. |
| [IErrorInfo interface](..\oaidl\nn-oaidl-ierrorinfo.md) | Provides detailed contextual error information. |
| [IRecordInfo interface](..\oaidl\nn-oaidl-irecordinfo.md) | Describes the structure of a particular UDT. |
| [ISupportErrorInfo interface](..\oaidl\nn-oaidl-isupporterrorinfo.md) | Ensures that error information can be propagated up the call chain correctly. Automation objects that use the error handling interfaces must implement ISupportErrorInfo. |
| [ITypeChangeEvents interface](..\oaidl\nn-oaidl-itypechangeevents.md) | Enables clients to subscribe to type change notifications on objects that implement the ITypeInfo, ITypeInfo2, ICreateTypeInfo, and ICreateTypeInfo2 interfaces. |
| [ITypeComp interface](..\oaidl\nn-oaidl-itypecomp.md) | The ITypeComp interface provides a fast way to access information that compilers need when binding to and instantiating structures and interfaces. |
| [ITypeInfo interface](..\oaidl\nn-oaidl-itypeinfo.md) | Used for reading information about objects. |
| [ITypeInfo2 interface](..\oaidl\nn-oaidl-itypeinfo2.md) | Used for reading information about objects. |
| [ITypeLib interface](..\oaidl\nn-oaidl-itypelib.md) | Represents a type library, the data that describes a set of objects. |
| [ITypeLib2 interface](..\oaidl\nn-oaidl-itypelib2.md) | Represents a type library, the data that describes a set of objects. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [LHashValOfName macro](..\oleauto\nf-oleauto-lhashvalofname.md) | Computes a hash value for a name. |
| [VarI4FromI4 macro](..\oleauto\nf-oleauto-vari4fromi4.md) | Converts an int value to a long value. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [ICreateErrorInfo::SetDescription](..\oaidl\nf-oaidl-icreateerrorinfo-setdescription.md) | Sets the textual description of the error. |
| [ICreateErrorInfo::SetGUID](..\oaidl\nf-oaidl-icreateerrorinfo-setguid.md) | Sets the globally unique identifier (GUID) of the interface that defined the error. |
| [ICreateErrorInfo::SetHelpContext](..\oaidl\nf-oaidl-icreateerrorinfo-sethelpcontext.md) | Sets the Help context identifier (ID) for the error. |
| [ICreateErrorInfo::SetHelpFile](..\oaidl\nf-oaidl-icreateerrorinfo-sethelpfile.md) | Sets the path of the Help file that describes the error. |
| [ICreateErrorInfo::SetSource](..\oaidl\nf-oaidl-icreateerrorinfo-setsource.md) | Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error. |
| [ICreateTypeInfo2::DeleteFuncDescByMemId](..\oaidl\nf-oaidl-icreatetypeinfo2-deletefuncdescbymemid.md) | Deletes the specified function description (FUNCDESC). |
| [ICreateTypeInfo2::DeleteFuncDesc](..\oaidl\nf-oaidl-icreatetypeinfo2-deletefuncdesc.md) | Deletes a function description specified by the index number. |
| [ICreateTypeInfo2::DeleteImplType](..\oaidl\nf-oaidl-icreatetypeinfo2-deleteimpltype.md) | Deletes the IMPLTYPE flags for the indexed interface. |
| [ICreateTypeInfo2::DeleteVarDescByMemId](..\oaidl\nf-oaidl-icreatetypeinfo2-deletevardescbymemid.md) | Deletes the specified VARDESC structure. |
| [ICreateTypeInfo2::DeleteVarDesc](..\oaidl\nf-oaidl-icreatetypeinfo2-deletevardesc.md) | Deletes the specified VARDESC structure. |
| [ICreateTypeInfo2::SetCustData](..\oaidl\nf-oaidl-icreatetypeinfo2-setcustdata.md) | Sets a value for custom data. |
| [ICreateTypeInfo2::SetFuncCustData](..\oaidl\nf-oaidl-icreatetypeinfo2-setfunccustdata.md) | Sets a value for custom data for the specified function. |
| [ICreateTypeInfo2::SetFuncHelpStringContext](..\oaidl\nf-oaidl-icreatetypeinfo2-setfunchelpstringcontext.md) | Sets a Help context value for a specified function. |
| [ICreateTypeInfo2::SetHelpStringContext](..\oaidl\nf-oaidl-icreatetypeinfo2-sethelpstringcontext.md) | Sets the context number for the specified Help string. |
| [ICreateTypeInfo2::SetImplTypeCustData](..\oaidl\nf-oaidl-icreatetypeinfo2-setimpltypecustdata.md) | Sets a value for custom data for the specified implementation type. |
| [ICreateTypeInfo2::SetName](..\oaidl\nf-oaidl-icreatetypeinfo2-setname.md) | Sets the name of the typeinfo. |
| [ICreateTypeInfo2::SetParamCustData](..\oaidl\nf-oaidl-icreatetypeinfo2-setparamcustdata.md) | Sets a value for the custom data for the specified parameter. |
| [ICreateTypeInfo2::SetVarCustData](..\oaidl\nf-oaidl-icreatetypeinfo2-setvarcustdata.md) | Sets a value for custom data for the specified variable. |
| [ICreateTypeInfo2::SetVarHelpStringContext](..\oaidl\nf-oaidl-icreatetypeinfo2-setvarhelpstringcontext.md) | Sets a Help context value for a specified variable. |
| [ICreateTypeInfo::AddFuncDesc](..\oaidl\nf-oaidl-icreatetypeinfo-addfuncdesc.md) | Adds a function description to the type description. |
| [ICreateTypeInfo::AddImplType](..\oaidl\nf-oaidl-icreatetypeinfo-addimpltype.md) | Specifies an inherited interface, or an interface implemented by a component object class (coclass). |
| [ICreateTypeInfo::AddRefTypeInfo](..\oaidl\nf-oaidl-icreatetypeinfo-addreftypeinfo.md) | Adds a type description to those referenced by the type description being created. |
| [ICreateTypeInfo::AddVarDesc](..\oaidl\nf-oaidl-icreatetypeinfo-addvardesc.md) | Adds a variable or data member description to the type description. |
| [ICreateTypeInfo::DefineFuncAsDllEntry](..\oaidl\nf-oaidl-icreatetypeinfo-definefuncasdllentry.md) | Associates a DLL entry point with the function that has the specified index. |
| [ICreateTypeInfo::LayOut](..\oaidl\nf-oaidl-icreatetypeinfo-layout.md) | Assigns VTBL offsets for virtual functions and instance offsets for per-instance data members, and creates the two type descriptions for dual interfaces. |
| [ICreateTypeInfo::SetAlignment](..\oaidl\nf-oaidl-icreatetypeinfo-setalignment.md) | Specifies the data alignment for an item of TYPEKIND=TKIND_RECORD. |
| [ICreateTypeInfo::SetDocString](..\oaidl\nf-oaidl-icreatetypeinfo-setdocstring.md) | Sets the documentation string displayed by type browsers. |
| [ICreateTypeInfo::SetFuncAndParamNames](..\oaidl\nf-oaidl-icreatetypeinfo-setfuncandparamnames.md) | Sets the name of a function and the names of its parameters to the specified names. |
| [ICreateTypeInfo::SetFuncDocString](..\oaidl\nf-oaidl-icreatetypeinfo-setfuncdocstring.md) | Sets the documentation string for the function with the specified index. |
| [ICreateTypeInfo::SetFuncHelpContext](..\oaidl\nf-oaidl-icreatetypeinfo-setfunchelpcontext.md) | Sets the Help context ID for the function with the specified index. |
| [ICreateTypeInfo::SetGuid](..\oaidl\nf-oaidl-icreatetypeinfo-setguid.md) | Sets the globally unique identifier (GUID) associated with the type description. |
| [ICreateTypeInfo::SetHelpContext](..\oaidl\nf-oaidl-icreatetypeinfo-sethelpcontext.md) | Sets the Help context ID of the type information. |
| [ICreateTypeInfo::SetImplTypeFlags](..\oaidl\nf-oaidl-icreatetypeinfo-setimpltypeflags.md) | Sets the attributes for an implemented or inherited interface of a type. |
| [ICreateTypeInfo::SetMops](..\oaidl\nf-oaidl-icreatetypeinfo-setmops.md) | Sets the marshaling opcode string associated with the type description or the function. |
| [ICreateTypeInfo::SetTypeDescAlias](..\oaidl\nf-oaidl-icreatetypeinfo-settypedescalias.md) | Sets the type description for which this type description is an alias, if TYPEKIND=TKIND_ALIAS. |
| [ICreateTypeInfo::SetTypeFlags](..\oaidl\nf-oaidl-icreatetypeinfo-settypeflags.md) | Sets type flags of the type description being created. |
| [ICreateTypeInfo::SetVarDocString](..\oaidl\nf-oaidl-icreatetypeinfo-setvardocstring.md) | Sets the documentation string for the variable with the specified index. |
| [ICreateTypeInfo::SetVarHelpContext](..\oaidl\nf-oaidl-icreatetypeinfo-setvarhelpcontext.md) | Sets the Help context ID for the variable with the specified index. |
| [ICreateTypeInfo::SetVarName](..\oaidl\nf-oaidl-icreatetypeinfo-setvarname.md) | Sets the name of a variable. |
| [ICreateTypeInfo::SetVersion](..\oaidl\nf-oaidl-icreatetypeinfo-setversion.md) | Sets the major and minor version number of the type information. |
| [ICreateTypeLib2::DeleteTypeInfo](..\oaidl\nf-oaidl-icreatetypelib2-deletetypeinfo.md) | Deletes a specified type information from the type library. |
| [ICreateTypeLib2::SetCustData](..\oaidl\nf-oaidl-icreatetypelib2-setcustdata.md) | Sets a value to custom data. |
| [ICreateTypeLib2::SetHelpStringContext](..\oaidl\nf-oaidl-icreatetypelib2-sethelpstringcontext.md) | Sets the Help string context number. |
| [ICreateTypeLib2::SetHelpStringDll](..\oaidl\nf-oaidl-icreatetypelib2-sethelpstringdll.md) | Sets the DLL name to be used for Help string lookup (for localization purposes). |
| [ICreateTypeLib::CreateTypeInfo](..\oaidl\nf-oaidl-icreatetypelib-createtypeinfo.md) | Creates a new type description instance within the type library. |
| [ICreateTypeLib::SaveAllChanges](..\oaidl\nf-oaidl-icreatetypelib-saveallchanges.md) | Saves the ICreateTypeLib instance following the layout of type information. |
| [ICreateTypeLib::SetDocString](..\oaidl\nf-oaidl-icreatetypelib-setdocstring.md) | Sets the documentation string associated with the library. |
| [ICreateTypeLib::SetGuid](..\oaidl\nf-oaidl-icreatetypelib-setguid.md) | Sets the universal unique identifier (UUID) associated with the type library. |
| [ICreateTypeLib::SetHelpContext](..\oaidl\nf-oaidl-icreatetypelib-sethelpcontext.md) | Sets the Help context ID for retrieving general Help information for the type library. |
| [ICreateTypeLib::SetHelpFileName](..\oaidl\nf-oaidl-icreatetypelib-sethelpfilename.md) | Sets the name of the Help file. |
| [ICreateTypeLib::SetLcid](..\oaidl\nf-oaidl-icreatetypelib-setlcid.md) | Sets the binary Microsoft national language ID associated with the library. |
| [ICreateTypeLib::SetLibFlags](..\oaidl\nf-oaidl-icreatetypelib-setlibflags.md) | Sets library flags. |
| [ICreateTypeLib::SetName](..\oaidl\nf-oaidl-icreatetypelib-setname.md) | Sets the name of the type library. |
| [ICreateTypeLib::SetVersion](..\oaidl\nf-oaidl-icreatetypelib-setversion.md) | Sets the major and minor version numbers of the type library. |
| [IDispatch::GetIDsOfNames](..\oaidl\nf-oaidl-idispatch-getidsofnames.md) | Maps a single member and an optional set of argument names to a corresponding set of integer DISPIDs, which can be used on subsequent calls to Invoke. |
| [IDispatch::GetTypeInfoCount](..\oaidl\nf-oaidl-idispatch-gettypeinfocount.md) | Retrieves the number of type information interfaces that an object provides (either 0 or 1). |
| [IDispatch::GetTypeInfo](..\oaidl\nf-oaidl-idispatch-gettypeinfo.md) | Retrieves the type information for an object, which can then be used to get the type information for an interface. |
| [IDispatch::Invoke](..\oaidl\nf-oaidl-idispatch-invoke.md) | Provides access to properties and methods exposed by an object. |
| [IEnumVARIANT::Clone](..\oaidl\nf-oaidl-ienumvariant-clone.md) | Creates a copy of the current state of enumeration. |
| [IEnumVARIANT::Next](..\oaidl\nf-oaidl-ienumvariant-next.md) | Retrieves the specified items in the enumeration sequence. |
| [IEnumVARIANT::Reset](..\oaidl\nf-oaidl-ienumvariant-reset.md) | Resets the enumeration sequence to the beginning. |
| [IEnumVARIANT::Skip](..\oaidl\nf-oaidl-ienumvariant-skip.md) | Attempts to skip over the next celt elements in the enumeration sequence. |
| [IErrorInfo::GetDescription](..\oaidl\nf-oaidl-ierrorinfo-getdescription.md) | Returns a textual description of the error. |
| [IErrorInfo::GetGUID](..\oaidl\nf-oaidl-ierrorinfo-getguid.md) | Returns the globally unique identifier (GUID) of the interface that defined the error. |
| [IErrorInfo::GetHelpContext](..\oaidl\nf-oaidl-ierrorinfo-gethelpcontext.md) | Returns the Help context identifier (ID) for the error. |
| [IErrorInfo::GetHelpFile](..\oaidl\nf-oaidl-ierrorinfo-gethelpfile.md) | Returns the path of the Help file that describes the error. |
| [IErrorInfo::GetSource](..\oaidl\nf-oaidl-ierrorinfo-getsource.md) | Returns the language-dependent programmatic ID (ProgID) for the class or application that raised the error. |
| [IRecordInfo::GetFieldNames](..\oaidl\nf-oaidl-irecordinfo-getfieldnames.md) | Gets the names of the fields of the record. |
| [IRecordInfo::GetFieldNoCopy](..\oaidl\nf-oaidl-irecordinfo-getfieldnocopy.md) | Returns a pointer to the value of a given field name without copying the value and allocating resources. |
| [IRecordInfo::GetField](..\oaidl\nf-oaidl-irecordinfo-getfield.md) | Returns a pointer to the VARIANT containing the value of a given field name. |
| [IRecordInfo::GetGuid](..\oaidl\nf-oaidl-irecordinfo-getguid.md) | Gets the GUID of the record type. |
| [IRecordInfo::GetName](..\oaidl\nf-oaidl-irecordinfo-getname.md) | Gets the name of the record type. |
| [IRecordInfo::GetSize](..\oaidl\nf-oaidl-irecordinfo-getsize.md) | Gets the number of bytes of memory necessary to hold the record instance. |
| [IRecordInfo::GetTypeInfo](..\oaidl\nf-oaidl-irecordinfo-gettypeinfo.md) | Retrieves the type information that describes a UDT or safearray of UDTs. |
| [IRecordInfo::IsMatchingType](..\oaidl\nf-oaidl-irecordinfo-ismatchingtype.md) | Determines whether the record that is passed in matches that of the current record information. |
| [IRecordInfo::PutFieldNoCopy](..\oaidl\nf-oaidl-irecordinfo-putfieldnocopy.md) | Passes ownership of the data to the assigned field by placing the actual data into the field. |
| [IRecordInfo::PutField](..\oaidl\nf-oaidl-irecordinfo-putfield.md) | Puts a variant into a field. |
| [IRecordInfo::RecordClear](..\oaidl\nf-oaidl-irecordinfo-recordclear.md) | Releases object references and other values of a record without deallocating the record. |
| [IRecordInfo::RecordCopy](..\oaidl\nf-oaidl-irecordinfo-recordcopy.md) | Copies an existing record into the passed in buffer. |
| [IRecordInfo::RecordCreateCopy](..\oaidl\nf-oaidl-irecordinfo-recordcreatecopy.md) | Creates a copy of an instance of a record to the specified location. |
| [IRecordInfo::RecordCreate](..\oaidl\nf-oaidl-irecordinfo-recordcreate.md) | Allocates memory for a new record, initializes the instance and returns a pointer to the record. |
| [IRecordInfo::RecordDestroy](..\oaidl\nf-oaidl-irecordinfo-recorddestroy.md) | Releases the resources and deallocates the memory of the record. |
| [IRecordInfo::RecordInit](..\oaidl\nf-oaidl-irecordinfo-recordinit.md) | Initializes a new instance of a record. |
| [ISupportErrorInfo::InterfaceSupportsErrorInfo](..\oaidl\nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo.md) | Indicates whether an interface supports the IErrorInfo interface. |
| [ITypeChangeEvents::AfterTypeChange](..\oaidl\nf-oaidl-itypechangeevents-aftertypechange.md) | Raised after a type has been changed. |
| [ITypeChangeEvents::RequestTypeChange](..\oaidl\nf-oaidl-itypechangeevents-requesttypechange.md) | Raised when a request has been made to change a type. The change can be disallowed. |
| [ITypeComp::BindType](..\oaidl\nf-oaidl-itypecomp-bindtype.md) | Binds to the type descriptions contained within a type library. |
| [ITypeComp::Bind](..\oaidl\nf-oaidl-itypecomp-bind.md) | Maps a name to a member of a type, or binds global variables and functions contained in a type library. |
| [ITypeInfo2::GetAllCustData](..\oaidl\nf-oaidl-itypeinfo2-getallcustdata.md) | Gets all custom data items for the library. |
| [ITypeInfo2::GetAllFuncCustData](..\oaidl\nf-oaidl-itypeinfo2-getallfunccustdata.md) | Gets all custom data from the specified function. |
| [ITypeInfo2::GetAllImplTypeCustData](..\oaidl\nf-oaidl-itypeinfo2-getallimpltypecustdata.md) | Gets all custom data for the specified implementation type. |
| [ITypeInfo2::GetAllParamCustData](..\oaidl\nf-oaidl-itypeinfo2-getallparamcustdata.md) | Gets all of the custom data for the specified function parameter. |
| [ITypeInfo2::GetAllVarCustData](..\oaidl\nf-oaidl-itypeinfo2-getallvarcustdata.md) | Gets the variable for the custom data. |
| [ITypeInfo2::GetCustData](..\oaidl\nf-oaidl-itypeinfo2-getcustdata.md) | Gets the custom data. |
| [ITypeInfo2::GetDocumentation2](..\oaidl\nf-oaidl-itypeinfo2-getdocumentation2.md) | Retrieves the documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file. |
| [ITypeInfo2::GetFuncCustData](..\oaidl\nf-oaidl-itypeinfo2-getfunccustdata.md) | Gets the custom data from the specified function. |
| [ITypeInfo2::GetFuncIndexOfMemId](..\oaidl\nf-oaidl-itypeinfo2-getfuncindexofmemid.md) | Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member). |
| [ITypeInfo2::GetImplTypeCustData](..\oaidl\nf-oaidl-itypeinfo2-getimpltypecustdata.md) | Gets the custom data of the implementation type. |
| [ITypeInfo2::GetParamCustData](..\oaidl\nf-oaidl-itypeinfo2-getparamcustdata.md) | Gets the custom data of the specified parameter. |
| [ITypeInfo2::GetTypeFlags](..\oaidl\nf-oaidl-itypeinfo2-gettypeflags.md) | Returns the type flags without any allocations. This returns a flag that expands the type flags without growing the TYPEATTR (type attribute). |
| [ITypeInfo2::GetTypeKind](..\oaidl\nf-oaidl-itypeinfo2-gettypekind.md) | Returns the TYPEKIND enumeration quickly, without doing any allocations. |
| [ITypeInfo2::GetVarCustData](..\oaidl\nf-oaidl-itypeinfo2-getvarcustdata.md) | Gets the custom data of the specified variable. |
| [ITypeInfo2::GetVarIndexOfMemId](..\oaidl\nf-oaidl-itypeinfo2-getvarindexofmemid.md) | Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member). |
| [ITypeInfo::AddressOfMember](..\oaidl\nf-oaidl-itypeinfo-addressofmember.md) | Retrieves the addresses of static functions or variables, such as those defined in a DLL. |
| [ITypeInfo::CreateInstance](..\oaidl\nf-oaidl-itypeinfo-createinstance.md) | Creates a new instance of a type that describes a component object class (coclass). |
| [ITypeInfo::GetContainingTypeLib](..\oaidl\nf-oaidl-itypeinfo-getcontainingtypelib.md) | Retrieves the containing type library and the index of the type description within that type library. |
| [ITypeInfo::GetDllEntry](..\oaidl\nf-oaidl-itypeinfo-getdllentry.md) | Retrieves a description or specification of an entry point for a function in a DLL. |
| [ITypeInfo::GetDocumentation](..\oaidl\nf-oaidl-itypeinfo-getdocumentation.md) | Retrieves the documentation string, the complete Help file name and path, and the context ID for the Help topic for a specified type description. |
| [ITypeInfo::GetFuncDesc](..\oaidl\nf-oaidl-itypeinfo-getfuncdesc.md) | Retrieves the FUNCDESC structure that contains information about a specified function. |
| [ITypeInfo::GetIDsOfNames](..\oaidl\nf-oaidl-itypeinfo-getidsofnames.md) | Maps between member names and member IDs, and parameter names and parameter IDs. |
| [ITypeInfo::GetImplTypeFlags](..\oaidl\nf-oaidl-itypeinfo-getimpltypeflags.md) | Retrieves the IMPLTYPEFLAGS enumeration for one implemented interface or base interface in a type description. |
| [ITypeInfo::GetMops](..\oaidl\nf-oaidl-itypeinfo-getmops.md) | Retrieves marshaling information. |
| [ITypeInfo::GetNames](..\oaidl\nf-oaidl-itypeinfo-getnames.md) | Retrieves the variable with the specified member ID or the name of the property or method and the parameters that correspond to the specified function ID. |
| [ITypeInfo::GetRefTypeInfo](..\oaidl\nf-oaidl-itypeinfo-getreftypeinfo.md) | If a type description references other type descriptions, it retrieves the referenced type descriptions. |
| [ITypeInfo::GetRefTypeOfImplType](..\oaidl\nf-oaidl-itypeinfo-getreftypeofimpltype.md) | If a type description describes a COM class, it retrieves the type description of the implemented interface types. |
| [ITypeInfo::GetTypeAttr](..\oaidl\nf-oaidl-itypeinfo-gettypeattr.md) | Retrieves a TYPEATTR structure that contains the attributes of the type description. |
| [ITypeInfo::GetTypeComp](..\oaidl\nf-oaidl-itypeinfo-gettypecomp.md) | Retrieves the ITypeComp interface for the type description, which enables a client compiler to bind to the type description's members. |
| [ITypeInfo::GetVarDesc](..\oaidl\nf-oaidl-itypeinfo-getvardesc.md) | Retrieves a VARDESC structure that describes the specified variable. |
| [ITypeInfo::Invoke](..\oaidl\nf-oaidl-itypeinfo-invoke.md) | Invokes a method, or accesses a property of an object, that implements the interface described by the type description. |
| [ITypeInfo::ReleaseFuncDesc](..\oaidl\nf-oaidl-itypeinfo-releasefuncdesc.md) | Releases a FUNCDESC previously returned by ITypeInfo |
| [ITypeInfo::ReleaseTypeAttr](..\oaidl\nf-oaidl-itypeinfo-releasetypeattr.md) | Releases a TYPEATTR previously returned by ITypeInfo |
| [ITypeInfo::ReleaseVarDesc](..\oaidl\nf-oaidl-itypeinfo-releasevardesc.md) | Releases a VARDESC previously returned by ITypeInfo |
| [ITypeLib2::GetAllCustData](..\oaidl\nf-oaidl-itypelib2-getallcustdata.md) | Gets all custom data items for the library. |
| [ITypeLib2::GetCustData](..\oaidl\nf-oaidl-itypelib2-getcustdata.md) | Gets the custom data. |
| [ITypeLib2::GetDocumentation2](..\oaidl\nf-oaidl-itypelib2-getdocumentation2.md) | Retrieves the library's documentation string, the complete Help file name and path, the localization context to use, and the context ID for the library Help topic in the Help file. |
| [ITypeLib2::GetLibStatistics](..\oaidl\nf-oaidl-itypelib2-getlibstatistics.md) | Returns statistics about a type library that are required for efficient sizing of hash tables. |
| [ITypeLib::FindName](..\oaidl\nf-oaidl-itypelib-findname.md) | Finds occurrences of a type description in a type library. This may be used to quickly verify that a name exists in a type library. |
| [ITypeLib::GetDocumentation](..\oaidl\nf-oaidl-itypelib-getdocumentation.md) | Retrieves the documentation string for the library, the complete Help file name and path, and the context identifier for the library Help topic in the Help file. |
| [ITypeLib::GetLibAttr](..\oaidl\nf-oaidl-itypelib-getlibattr.md) | Retrieves the structure that contains the library's attributes. |
| [ITypeLib::GetTypeComp](..\oaidl\nf-oaidl-itypelib-gettypecomp.md) | Enables a client compiler to bind to the types, variables, constants, and global functions for a library. |
| [ITypeLib::GetTypeInfoCount](..\oaidl\nf-oaidl-itypelib-gettypeinfocount.md) | Provides the number of type descriptions that are in a type library. |
| [ITypeLib::GetTypeInfoOfGuid](..\oaidl\nf-oaidl-itypelib-gettypeinfoofguid.md) | Retrieves the type description that corresponds to the specified GUID. |
| [ITypeLib::GetTypeInfoType](..\oaidl\nf-oaidl-itypelib-gettypeinfotype.md) | Retrieves the type of a type description. |
| [ITypeLib::GetTypeInfo](..\oaidl\nf-oaidl-itypelib-gettypeinfo.md) | Retrieves the specified type description in the library. |
| [ITypeLib::IsName](..\oaidl\nf-oaidl-itypelib-isname.md) | Indicates whether a passed-in string contains the name of a type or member described in the library. |
| [ITypeLib::ReleaseTLibAttr](..\oaidl\nf-oaidl-itypelib-releasetlibattr.md) | Releases the TLIBATTR originally obtained from GetLibAttr. |
